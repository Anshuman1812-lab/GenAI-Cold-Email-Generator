# ImpactMailer

![image](https://github.com/user-attachments/assets/dbca4d47-9e4b-45be-b6b5-7e1267eb9517)

## Output
```bash
Subject: Application for Engineer Access Identity Management Associate Role

Dear Hiring Manager,

I am excited to apply for the Engineer Access Identity Management Associate position at BlackRock, where I can utilize
my expertise in Access and Identity Management to support IAM functions in Microsoft Azure and AWS environments. With
over 5 years of experience in Access and Identity Management, I am confident that my skills and passion for cloud
security governance practices make me an ideal candidate for this role.

Throughout my career, I have gained extensive experience working with IAM within Microsoft Azure and Amazon Web
Services (AWS) environments, with a strong focus on Privileged Identity Management (PIM) and Role-Based Access Control
(RBAC). My expertise in Azure DevOps, Terraform, Python scripting, and PowerShell has enabled me to craft and maintain
roles, permissions, and entitlements for various businesses and departments. I am well-versed in cloud security
governance practices and have experience with IAM policy and document preparation.

I would like to highlight some of my relevant projects that demonstrate my capabilities:

* GDPR-Android-Threat-Analysis (https://github.com/Anshuman1812-lab/GDPR-Android-Threat-Analysis): This project
showcases my ability to analyze and identify potential threats in Android applications, ensuring compliance with GDPR
regulations.
* OSINT-Gathering (https://github.com/Anshuman1812-lab/OSINT-Gathering): This project demonstrates my skills in
gathering and analyzing open-source intelligence, which can be applied to identity management and access control.
* The Cyber Trap (https://medium.com/@anshumansingh1/the-cyber-trap-c8467168663c): This article highlights my
understanding of cloud security risks and the importance of implementing robust identity and access management
practices.

I am excited about the opportunity to join BlackRock and contribute my expertise to support the company's cloud
identity access management functions. Thank you for considering my application. I look forward to discussing my
qualifications further.

Best regards,
Anshuman Singh
```

## 🚀 Overview
ImpactMailer is a **GenAI-based Cold Email Generator** is a sophisticated solution designed to simplify the process of creating personalized cold emails for job postings. By utilizing advanced technologies like **LangChain, ChromaDB, and Generative AI**, this project enables efficient email generation while maintaining a high degree of customization and relevance.

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

### ✉️ Tailored Email Generation:
- Leverages **Generative AI (GenAI)**, specifically **Llama 3.1** of the Llama series of large language models (LLMs) from Meta, to craft persuasive and professional emails.
- Integrates your professional expertise, highlighting the the ability to fulfill the client's needs.
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
git clone https://github.com/Anshuman1812-lab/ImpactMailer.git
cd ImpactMailer
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
ImpactMailer/
├── chains.py          # Core logic for job extraction and email generation using LangChain
├── main.py            # Entry point for the Streamlit application
├── portfolio.py       # Handles portfolio data loading and skill-based querying
├── utils.py           # Utility functions for text cleaning and preprocessing
├── requirements.txt   # List of Python dependencies required for the project
├── my_portfolio.csv   # CSV file containing portfolio projects and links
├── .env               # Environment file for storing sensitive keys (not included in the repository)
```
