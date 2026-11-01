# Book Your Admissions

An AI-powered college search and admission assistance platform designed to help students discover colleges, explore courses, and access admission information.

## Features

- College search by course and location.
- Eligibility text filtering.
- Fee sorting with missing values handled.
- College information retrieval from available brochures.
- Gradio-based user interface.
- FastAPI search endpoint.
- Automated admission deadline reminders using n8n and Gmail.
- English and Telugu chatbot interface.

## Technology Stack

- Python
- Pandas
- Gradio
- FastAPI
- Google Sheets
- n8n
- Gmail
- ngrok (development tunnelling)

## Project Dataset

The prototype contains 15 college-course records representing five colleges in Andhra Pradesh.

## Project Structure

- `app/` – Backend application
- `data/` – College dataset
- `notebooks/` – Development notebook
- `tests/` – Test reports

## Current Status

Working prototype. Data verification, integrated testing, and permanent deployment are ongoing.

## Running the Project

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the FastAPI application:

```bash
uvicorn app.main:app --reload
```

## Important

College fees, eligibility criteria, and admission deadlines must be verified against official institutional sources. Missing information is not treated as zero or assumed.

## Future Improvements

- Complete official college data verification.
- Improve recommendation functionality.
- Add persistent database storage.
- Deploy frontend and backend.
- Add automated tests and authentication.

## Author

Desu Rajendra Kumar
