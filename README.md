# HR-Recruitment-AI-System
End-to-end AI-powered HR recruitment system using Gemini File Search–based Retrieval-Augmented Generation (RAG), Supabase, and LangGraph.
🧠 HR Recruitment AI System

An end-to-end AI-powered HR recruitment pipeline that automates resume ingestion, candidate screening, and interview evaluation using Gemini File Search–based Retrieval-Augmented Generation (RAG), Supabase, and LangGraph — built entirely in Python.

🚀 Key Features

📥 Batch Resume Ingestion

Fetches resumes from Supabase Storage

Uploads them to Gemini File Search Store with metadata

Prevents duplicate processing using flags

🔍 AI Resume Screening (RAG)

Screens only uploaded resumes

Matches candidates strictly against job descriptions

No hallucinations or external knowledge usage

🎤 Interview Intelligence & Scoring

Evaluates interview transcripts using AI

Generates score, performance summary, and hiring status

Automatically updates results back to database

🔄 Orchestrated Pipeline

Entire flow managed using LangGraph

Modular agent-based architecture



🧩 Agents Overview
1️⃣ CV Ingestion Agent

Fetches pending resumes (rag_uploaded = false)

Processes resumes in configurable batches

Uploads resumes to Gemini RAG store with metadata:

application_id

candidate_id

job_id

2️⃣ Resume Screening Agent

Uses Gemini File Search for retrieval

Screens candidates strictly from uploaded resumes

Returns top N candidates per job description

Designed for HR-friendly output

3️⃣ Interview Scoring Agent

Reads interview transcripts from Supabase

Evaluates candidates using AI interviewer logic

Generates:

Score (0–10)

Performance (Strong / Average / Weak)

Status (Select / Hold / Reject)

⚙️ Tech Stack Used

Python

Supabase

Database

Storage

Google Gemini API

Gemini 2.5 Flash

File Search (RAG)

LangGraph

Pipeline orchestration

dotenv

Environment variable management



📁 Project Structure
01_setup.ipynb                  # Environment setup & utilities
02_Resume_Indexing_Agent.ipynb  # CV ingestion agent
03_Resume_Screening_Agent.ipynb # Resume screening agent
04_Interview_Intelligence_Agent.ipynb # Interview scoring agent
05_run_pipeline.ipynb           # End-to-end pipeline execution

▶️ How the Pipeline Runs

1.Ingest resumes in batches from Supabase

2.Upload resumes to Gemini File Search Store

3.Screen candidates based on job description

4.Evaluate interview transcripts

5.Update final hiring decision in database

🎯 Why This Project Matters

Demonstrates real-world RAG system design

Scalable for thousands to millions of resumes

Clean separation of ingestion, retrieval, reasoning, and decision-making

Ideal for AI/ML Engineer, Data Scientist, and Backend AI roles

🧪 Future Enhancements

Confidence score aggregation

JSON & table-based outputs

Job and department-based filtering

Automated interview scheduling

ATS-style ranking and analytics dashboard

🙌 Author

Mohd Shahbaz Khan
Aspiring Data Scientist | AI Engineer
Focused on building production-ready AI systems

