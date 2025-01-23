# GenAI Cold Email Generator

## 🚀 Overview
The **GenAI-based Cold Email Generator** is a sophisticated solution designed to simplify the process of creating personalized cold emails for job postings. By utilizing advanced technologies like **LangChain, ChromaDB, and Generative AI**, this project enables efficient email generation while maintaining a high degree of customization and relevance.

This tool extracts detailed job descriptions from company websites and generates professional, tailored emails that align with the specific needs of the roles. By integrating a portfolio query system, the emails also showcase relevant projects to enhance their impact.


## 🌟 Key Features
### 🔍 Intelligent Job Post Extraction:
- Automatically scrapes job postings from any provided URL.
- Extracts key details like:
  - **Role:** The position being advertised.
  - **Experience:** Required qualifications and background.
  - **Skills:** Technical or soft skills specified in the job description.
  - **Description:** A detailed summary of the job posting.
- Output is structured in a clean JSON format for further processing.

### ✉️ Tailored Cold Email Generation:
- Leverages **Generative AI (GenAI)**, specifically **Llama 3.1** of the Llama series of large language models (LLMs) from Meta, to craft persuasive and professional cold emails.
- Ensures every email is unique, personalized, and highly relevant to the job posting.

### 📂 Portfolio Integration:
- Dynamically attaches the most relevant project links from a CSV-based portfolio.
- Uses **ChromaDB** for vector-based similarity search, ensuring the attached links align with the required skills and expertise for the job.

### 🌐 User-Friendly Web Interface:
- Powered by **Streamlit**, the app offers a clean and intuitive interface for users.
- Simply input a URL, and the app handles the rest—scraping data, generating emails, and showcasing the output.


## 🛠️ Technologies Used

|**Technology**       | Purpose                                              |
|:--------------------|:-----------------------------------------------------|
| **Python**          | Primary programming language.                        |
| **LangChain**       | Handles natural language processing and logic flow.  |
| **Generative AI**   | Creates dynamic, professional email content.         |
| **Streamlit**       | Builds an interactive and user-friendly interface.   |
| **ChromaDB**        | Enables skill-based portfolio querying.              |
| **Pandas**          | Facilitates data manipulation from CSV files.        |
| **Selenium**        | Provides web scraping capabilities.                  |
| **dotenv**          | Manages secure storage of environment variables.     |


## 📖 Detailed Installation Instructions
To set up the project on your local machine, follow these steps:
### 1. Clone the Repository:
```bash
git clone https://github.com/your_username/cold-email-generator.git
cd cold-email-generator
```

### 2. Install Dependencies:
Install all the required Python libraries listed in `requirements.txt`:
```bash
pip install -r requirements.txt
```

### 3. Set Environment Variables:
Create a `.env` file in the root directory and add your GROQ API Key:
```bash
GROQ_API_KEY=<your_groq_api_key>
```

### 4. Prepare Portfolio Data:
Place your portfolio CSV file in the default directory: `app/resource/my_portfolio.csv`.
Ensure the file contains columns for project descriptions (`Techstack`) and links (`Links`).

### 5. Run the Application:
Start the Streamlit app with the following command:
```bash
streamlit run main.py
```


## 🎯 How to Use the Application
1. Launch the Streamlit app by running the command above.
2. Enter the URL of a job posting (e.g., https://jobs.nike.com/job/R-45889?from=job%20search%20funnel) into the input field.
3. Click the Submit button to start the process.
4. The app will:
  - Scrape and clean the job data.
  - Use the portfolio to find relevant project links.
  - Generate a professional email, displayed in markdown format.
5. Review and copy the generated email for immediate use.


## 📂 Project Structure
The project is organized as follows:

```plaintext
cold-email-generator/
├── chains.py          # Core logic for job extraction and email generation using LangChain
├── main.py            # Entry point for the Streamlit application
├── portfolio.py       # Handles portfolio data loading and skill-based querying
├── utils.py           # Utility functions for text cleaning and preprocessing
├── requirements.txt   # List of Python dependencies required for the project
├── my_portfolio.csv   # CSV file containing portfolio projects and links
├── .env               # Environment file for storing sensitive keys (not included in the repository)
```
