📘 Personalized AI Study Assistant

An AI-powered study assistant that analyzes a student’s past performance, syllabus, and goals to generate personalized daily study plans and practice questions. Built for hackathons and academic competitions, this project demonstrates how AI can enhance exam preparation and optimize learning outcomes.

🚀 Features

🎯 Personalized Study Planner: Generates customized daily study schedules based on syllabus coverage and performance history.
📊 Performance Analytics: Provides insights into strong and weak subjects using past test results.
🤖 AI-Powered Question Generator: Suggests practice questions and quizzes dynamically using NLP.
📅 Smart Reminders: Sends study reminders and breaks suggestions to prevent burnout.
📈 Progress Tracker: Visual dashboard to monitor learning progress and exam readiness.

🏗️ System Architecture

The project follows a modular microservices-like architecture:

Data Layer: Stores syllabus, performance records, and user preferences.

Model Layer: ML/NLP models for analyzing weak areas and generating practice questions.

Backend API: FastAPI server that provides endpoints for study plan generation and analytics.

Frontend Dashboard: Streamlit app that interacts with the backend and displays the personalized study interface.

ai-study-assistant/
│
├── data/
│   └── student_performance.csv          # Sample past performance data
│
├── models/
│   ├── study_plan_generator.py          # Logic for creating personalized plans
│   └── question_generator.py            # Simple NLP-based practice question generator
│
├── backend/
│   ├── serve_model.py                   # FastAPI application
│   └── requirements.txt                 # Backend dependencies
│
├── dashboard/
│   ├── app_streamlit.py                 # Streamlit dashboard
│   └── requirements.txt                 # Frontend dependencies
│
├── scripts/
│   └── generate_dummy_data.py           # Script to generate sample student data
│
├── architecture_diagram.png             # System architecture diagram
└── README.md


🖥️ Steps to Run in VS Code

1. Create & Activate Virtual Environment

Run this in the VS Code terminal:

python -m venv venv


Activate it:

On Windows (PowerShell):

venv\Scripts\activate


On Linux/Mac:

source venv/bin/activate

2. Install Dependencies

Install for both backend and frontend.

Backend
cd backend
pip install -r requirements.txt
cd ..

Frontend
cd dashboard
pip install -r requirements.txt
cd ..

3. Run Backend (FastAPI Server)
cd backend
uvicorn serve_model:app --reload


Keep this terminal running (it hosts your API).

FastAPI will start at 👉 http://127.0.0.1:8000
.

4. Run Frontend (Streamlit Dashboard)

Open a new terminal in VS Code (don’t close backend).

cd dashboard
streamlit run app_streamlit.py


This will launch the dashboard in your browser at 👉 http://localhost:8501
.

5. View & Use App

The dashboard will show your study plan and analytics.

The backend provides AI-powered recommendations in real-time.
