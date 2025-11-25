🎯 VocaPrep – AI-Powered Interview Preparation Platform

VocaPrep is an intelligent, end-to-end interview preparation platform built using Django, MySQL, Groq LLM, and Whisper Speech-to-Text, designed to help users practice interviews, receive AI-driven feedback, track performance, and improve communication skills.

It includes authentication, profile management, speech analysis, LLM-based scoring, and email verification — packed inside a modern Django application.

📘 Table of Contents

Overview
<img width="1900" height="906" alt="Screenshot 2025-11-25 154957" src="https://github.com/user-attachments/assets/62c4531c-da9e-48a7-84b9-60a7ff122e27" />


Tech Stack

Key Features

System Architecture

Module-wise Explanation

AI Pipeline (Whisper + LLM)

Setup Instructions

Environment Variables

Project Structure

Future Enhancements

Screenshots

Contact

🌟 Overview

VocaPrep is a smart interview preparation system that allows users to:

✔ Practice interview questions
✔ Record answers using microphone
✔ Convert speech → text using Whisper
✔ Process answers using Groq LLM
✔ Receive AI-generated feedback, scoring & suggestions
✔ Manage profile and authentication
✔ Verify email before login

The goal is to deliver a personal AI interview coach that helps students and job-seekers practice effectively.

⚙️ Tech Stack
Layer	Technology
Backend	Django 4.x, Python 3.11
Database	MySQL
AI Engines	Groq LLM, Whisper STT
Frontend	HTML, CSS, JavaScript
Auth	Django Auth, token-based email verification
Deployment	PythonAnywhere / Render (planned)
🚀 Key Features
🎤 AI-Powered Interview Practice

Users can record voice responses

Answers are converted using Whisper STT

Groq LLM evaluates answers with:
✔ Clarity Score
✔ Grammar Suggestions
✔ Technical Depth Feedback
✔ Confidence Score
✔ Final Recommendation

🧠 AI Feedback Engine

Uses Groq LLM to analyze user responses

Provides structured JSON output

Gives personalized improvement advice

👤 Authentication & User Management

Register with email

Email verification using token

Login / Logout

Profile page

📬 Email Verification

OTP / Token-based activation

Prevents unverified logins

📊 Dashboard

Shows user details

Interview practice history (optional)

Quick actions & shortcuts

🎨 Modern, Responsive UI

Clean layout using HTML + CSS

JavaScript for audio recording & interactions

🧩 System Architecture
VocaPrep/
│── ai_interview_assistant/
│   ├── core/                 → Views, STT, LLM, logic
│   ├── templates/            → HTML templates
│   ├── static/               → CSS, JS
│   ├── settings.py           → Config (no secrets stored)
│   ├── urls.py
│   └── wsgi.py
│
│── manage.py
└── requirements.txt

🧱 Module-wise Explanation
🔹 1. Core Module

Handles:

AI evaluation logic

Whisper speech-to-text

LLM feedback generation

Dashboard

Home page

Key Files
File	Purpose
whisper_stt.py	Converts audio to text
llm_feedback.py	LLM scoring & analysis
views.py	Web views
utils.py	Helper functions
🔹 2. Authentication Module

Manages:

Registration

Email verification

Login/logout

Profile

Features:

Secure token generation

Auto email sending

Verification templates

🔹 3. Templates

Structured HTML components:

templates/
│── base.html
│── login.html
│── register.html
│── dashboard.html
│── verify_success.html
│── verify_fail.html
│── verify_sent.html
│── components/

🤖 AI Pipeline (Whisper + LLM)
🎤 STEP 1 — User records answer

Browser → JavaScript Audio Recorder → Backend

🔊 STEP 2 — Whisper STT

Audio → Whisper → Text transcription

🤖 STEP 3 — LLM Evaluation (Groq)

Text → Groq model → Feedback JSON

📊 STEP 4 — Score & Feedback

Returned to UI as structured result.

🛠 Setup Instructions
1️⃣ Clone Repo
git clone https://github.com/NAGENDRANADH02/VocaPrep.git
cd VocaPrep

2️⃣ Create Virtual Environment
python -m venv venv
venv\Scripts\activate  # Windows
source venv/bin/activate  # Linux/Mac

3️⃣ Install Dependencies
pip install -r requirements.txt

4️⃣ Configure Database

Edit MySQL credentials in settings.py
(ENV-based — no secrets inside repo)

5️⃣ Run Migrations
python manage.py makemigrations
python manage.py migrate

6️⃣ Create Superuser
python manage.py createsuperuser

7️⃣ Start Server
python manage.py runserver


Visit:
👉 http://127.0.0.1:8000/

🔑 Environment Variables

Create a .env (not committed to GitHub):

DJANGO_SECRET_KEY=your_secret_here
MYSQL_PASSWORD=your_password
EMAIL_HOST_USER=xxxx@gmail.com
EMAIL_HOST_PASSWORD=xxxx
GROQ_API_KEY=your_groq_key

📸 Screenshots

<img width="1915" height="898" alt="Screenshot 2025-11-25 155037" src="https://github.com/user-attachments/assets/680bffcc-4b23-4fbc-8af9-f0bab7bf1192" />
<img width="1897" height="906" alt="Screenshot 2025-11-25 155104" src="https://github.com/user-attachments/assets/5c02dcfa-7809-4680-a844-583b8f037b23" />

