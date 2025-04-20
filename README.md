# InsightBridge: AI-Powered Business Intelligence Assistant

InsightBridge is an AI-powered business intelligence assistant designed to enhance decision-making and automate data analysis tasks. This project combines advanced machine learning, natural language processing (NLP), and cloud technologies to offer an intuitive platform for businesses to extract valuable insights from their data.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Installation](#installation)
---

## Overview

InsightBridge is built with a **React frontend** and a **FastAPI backend**, which work seamlessly together to provide an interactive and dynamic interface for business intelligence tasks. Users can upload datasets, perform exploratory data analysis (EDA), apply automated machine learning (AutoML), and generate insightful reports with the help of GPT-powered Q&A features.

---

## Features

- **Data Upload**: Allows users to upload CSV files and other data formats for analysis.
- **Exploratory Data Analysis (EDA)**: Generates statistical summaries, data visualizations, and detects outliers.
- **Automated Machine Learning (AutoML)**: Automatically selects the best model based on dataset characteristics.
- **Question-Answering (Q&A) with GPT**: Users can ask questions related to their data, and the system will provide answers using GPT.
- **Report Generation**: Automatically generates PDF reports based on the analysis and predictions.
- **Dashboard**: Interactive dashboard for visualizing data and model performance.

---

## Tech Stack

### Frontend
- **React.js**: A JavaScript library for building user interfaces.
- **Tailwind CSS**: A utility-first CSS framework for styling.
- **Axios**: Promise-based HTTP client for making API requests.
  
### Backend
- **FastAPI**: A modern, fast (high-performance) web framework for building APIs with Python 3.7+.
- **PyCaret**: A low-code machine learning library to streamline the process of building ML models.
- **Pydantic**: Data validation and settings management using Python type annotations.
  
### Database
- **MongoDB**: NoSQL database for storing user data and models (optional).

### DevOps
- **Docker**: Containerization for easy deployment and scalability.
- **Docker Compose**: To run multiple services like frontend, backend, and database together.

---

## Project Structure

Here is the structure of the `InsightBridge` project:

```bash
InsightBridge-Project/
├── frontend/                       # React frontend
│   ├── public/                     # Static assets
│   ├── src/
│   │   ├── assets/                 # Images, logos, icons, etc.
│   │   ├── components/             # Reusable components (Navbar, Sidebar, Chart, etc.)
│   │   ├── pages/                  # Pages (UploadPage, Dashboard, LoginPage, etc.)
│   │   ├── services/               # Axios API handlers
│   │   ├── utils/                  # Helper functions
│   │   ├── App.js                  # Main component
│   │   └── index.js                # React entry point
│   ├── tailwind.config.js
│   ├── package.json
│   └── .env                        # React environment variables

├── backend/                        # FastAPI backend
│   ├── app/
│   │   ├── api/                    # All API routes
│   │   │   ├── upload.py
│   │   │   ├── eda.py
│   │   │   ├── automl.py
│   │   │   ├── qna_gpt.py
│   │   │   └── report.py
│   │   ├── core/                   # Core configurations, utilities
│   │   │   ├── config.py
│   │   │   └── utils.py
│   │   ├── models/                 # DB models/schemas (Pydantic)
│   │   ├── services/               # ML, GPT, EDA logic
│   │   ├── templates/              # Jinja2 templates for PDFs
│   │   └── main.py                 # FastAPI entry point
│   ├── Dockerfile
│   ├── requirements.txt
│   └── .env                        # Backend environment variables

├── ml_models/                      # Saved PyCaret models
│   ├── classification/
│   └── regression/

├── docker-compose.yml              # (Optional) To run frontend + backend + MongoDB together
├── README.md                       # Project overview & setup guide
├── .gitignore
└── LICENSE
```


---

## Installation

To run this project locally, follow these steps:

### Prerequisites
- **Node.js** (for frontend)
- **Python 3.x** (for backend)
- **Docker** (for containerization)

### Frontend Installation

1. Navigate to the `frontend` directory:
   ```bash
   cd frontend
2. Install the dependencies:
   ```bash
   npm install

### Backend Installation

1. Navigate to the backend directory:
   ```bash
    cd backend

3. Create a virtual environment:
   ```bash
    python -m venv venv

5. Activate the virtual environment:
 - Windows:
  .\venv\Scripts\activate
 - Linux/Mac:
  source venv/bin/activate

4. Install the Python dependencies:
   ```bash
   pip install -r requirements.txt

## Contributing

We welcome contributions! Feel free to fork the repository and submit pull requests. For any bugs or feature requests, please open an issue.
