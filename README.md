# Semiautomatic Job Post Application AI Agent

## Overview

The Semiautomatic Job Post Application AI Agent is a Jupyter Notebook-based solution that streamlines the job application process. By leveraging the Deepseek API, this agent processes job descriptions, generates targeted Q&A prompts to refine your resume, and ultimately produces customized CVs and cover letters for each job post.

## Features

- **Automated Job Post Processing:**  
  Reads job descriptions stored as `.txt` files in the `posts` folder.

- **Keyword Q&A Generation:**  
  Uses Deepseek API to generate questions and potential answers regarding key resume keywords. This helps identify gaps in your current resume and suggests improvements.

- **Manual Review Stage:**  
  Pauses the workflow to allow for human intervention—enabling you to review and modify the generated Q&A files before proceeding.

- **General Resume Enhancement:**  
  Utilizes Deepseek to rewrite and augment a general resume from `gen_resume.txt` to create a modern and optimized version.

- **Customized CV and Cover Letter Creation:**  
  Generates individual CVs and cover letters in DOCX format for each job post. The output files are formatted to be easily parsed by job boards like Indeed and Careerbeacon, with structured sections for job experience and education.

- **Timestamped Outputs:**  
  Each generated CV and cover letter file is appended with the current date for version control.

## Workflow

1. **Load Job Posts:**  
   The agent reads all `.txt` files from the `posts` folder and stores each job description.

2. **Generate Q&A for Keywords:**  
   For every job post, the agent sends a prompt to the Deepseek API to generate relevant questions and answers about resume keywords. The output is saved as a corresponding `_qa.txt` file in the `questions` folder.

3. **Manual Review:**  
   Execution pauses to allow you to inspect and adjust the generated Q&A files as needed.

4. **Update General Resume:**  
   The agent uses Deepseek to rewrite and augment the existing general resume (`gen_resume.txt`).

5. **Generate Individual CVs and Cover Letters:**  
   For each job post, the agent combines the job description, the reviewed Q&A responses, and the updated general resume. It then generates tailored CVs and cover letters, saving them as DOCX files with filenames that include the job post name, document type, and current date.

## Technology & Dependencies

- **Python & Jupyter Notebook:**  
  Core development environment and execution platform.

- **Deepseek API:**  
  Provides the natural language processing capabilities via an OpenAI-compatible interface.

- **python-docx:**  
  Used for creating and modifying Microsoft Word (.docx) files.

- **Standard Python Libraries:**  
  - `os` for file and folder operations  
  - `datetime` for timestamping outputs

## Setup Instructions

1. **Clone the Repository:**  
   Download or clone the repository containing the Jupyter Notebook and the required folders (`posts` and `questions`).

2. **Install Dependencies:**  
   Ensure you have Python installed and run:
   ```bash
   pip install openai python-docx