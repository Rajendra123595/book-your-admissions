# Book Your Admissions 🎓

**An AI-powered college search and admission assistance platform** designed to help students discover colleges, explore courses, understand eligibility requirements and access admission-related information.

## 📌 Project Overview

Book Your Admissions aims to simplify the college admission discovery process by bringing college information, brochure-based question answering and admission deadline notifications into one platform.

The project combines Python-based data processing, a Gradio interface, FastAPI endpoints and n8n workflow automation.

## ✨ Features

### 1. College Search
- Search colleges by course and location.
- Filter colleges using eligibility information.
- Display college names, courses, locations and official websites.
- Handle missing fee and eligibility information without assuming values.
- Support fee-based sorting where data is available.

### 2. AI-Based Brochure Information Retrieval
- Retrieve information from uploaded college brochures.
- Answer questions using available brochure content.
- Support English and Telugu chatbot interaction.
- Indicate when information cannot be found in the available documents.

### 3. Admission Deadline Notifications
- Schedule automatic deadline checks using n8n.
- Retrieve college deadline records from Google Sheets.
- Identify upcoming admission deadlines.
- Use conditional logic to determine whether notifications are required.
- Send reminder emails through Gmail.

### 4. Web Interface and API
- Gradio-based student interface.
- FastAPI backend for college search.
- JSON-based API responses.
- ngrok tunnelling for development and external API testing.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Application logic |
| Pandas | Dataset processing and filtering |
| Gradio | User interface |
| FastAPI | Backend API |
| Pydantic | API request validation |
| Google Colab | Development environment |
| Google Sheets | College and deadline records |
| n8n | Workflow automation |
| Gmail | Email notifications |
| ngrok | Development API tunnelling |

## 🏗️ System Architecture

### College Search Flow

```text
Student
   |
   v
Gradio Interface
   |
   v
FastAPI Endpoint
   |
   v
College Search Function
   |
   v
Pandas Data Processing
   |
   v
College Dataset (CSV)
   |
   v
Filtered College Results
```

### Admission Deadline Reminder Flow

```text
Schedule Trigger
       |
       v
Google Sheets
       |
       v
Deadline Checking
       |
       v
IF Condition
       |
       +------ True ------> Gmail Notification
       |
       +------ False -----> No Notification
```

### Brochure Retrieval Flow

```text
Student Question
       |
       v
Brochure Retrieval
       |
       v
Relevant Document Content
       |
       v
Answer or Information Not Available
```

## 📊 Project Dataset

The current prototype contains:

- **15 college-course records**
- **5 colleges**
- Focus on B.Tech CSE records in Andhra Pradesh.

Dataset fields include:

- `college_name`
- `course_name`
- `location`
- `eligibility`
- `annual_fee_inr`
- `official_url`
- `checked_on`
- `application_deadline`
- `deadline_source_url`

Some fee, eligibility and deadline fields are incomplete or awaiting verification. The application should not present unverified information as confirmed admission facts.

## 📁 Repository Structure

```text
book-your-admissions/
│
├── n8n/
│   └── deadline_reminder_workflow.json
│
├── Book_Your_Admissions_AI_ipynb_.ipynb
│
├── colleges.csv
│
├── requirements.txt
│
├── README.md
│
└── .gitignore
```

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Rajendra123595/book-your-admissions.git
```

### 2. Open the project

```bash
cd book-your-admissions
```

### 3. Create a virtual environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Run the development notebook

Open `Book_Your_Admissions_AI_ipynb_.ipynb` in Google Colab or Jupyter Notebook.

Upload or provide access to the college dataset and execute the required notebook cells in order.

**Note:** The current implementation is notebook-based. FastAPI and Gradio are run through the development notebook; standalone deployment files such as `app/main.py` are not yet included.

## 🔄 n8n Workflow

The exported workflow is available at:

`n8n/deadline_reminder_workflow.json`

The workflow includes:

1. Schedule Trigger.
2. Google Sheets integration.
3. Deadline-checking code.
4. IF condition.
5. Gmail notification
