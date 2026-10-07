# Dossier — Adaptive Study Tutor

**TechVortex '26 · AI Education & Personalized Learning**

An intelligent **Adaptive Study Tutor** that continuously understands a student's learning progress, identifies weak areas, generates personalized study plans, adapts explanations to the student's level, and uses **agentic AI** to autonomously manage the learning workflow.

Instead of providing the same material to every student, the system builds a **dynamic learning path** based on performance, confidence, previous mistakes, study history, and upcoming academic goals.

The tutor acts as a **personal AI study agent** — it can assess, plan, teach, test, analyze, and adapt without requiring the student to manually configure every step.

## Core Workflow

```text
Student
   ↓
Profile + Academic Goals
   ↓
Diagnostic Assessment
   ↓
Knowledge / Performance Analysis
   ↓
Weak Topic Identification
   ↓
Adaptive Study Planner
   ↓
AI Tutor Agent
   ├── Explain
   ├── Give Examples
   ├── Generate Notes
   └── Answer Questions
   ↓
Adaptive Quiz Agent
   ↓
Performance Evaluation
   ↓
Mistake + Knowledge-Gap Analysis
   ↓
Plan Re-optimization
   ↓
Personalized Learning Path
   ↓
Progress Dashboard
```

## Agentic AI Architecture

The platform uses multiple specialized AI agents instead of a single generic chatbot.

### 1. **Learner Profiling Agent**
Builds and continuously updates the student's learning profile using:

- Quiz performance
- Topic-wise accuracy
- Previous mistakes
- Study frequency
- Response time
- Confidence level
- Learning preferences

The agent maintains a dynamic representation of **what the student knows, what they partially understand, and what they need to learn next**.

### 2. **Assessment Agent**
Automatically evaluates the student's current knowledge.

It can:

- Generate diagnostic questions
- Select questions based on difficulty
- Evaluate answers
- Detect recurring mistakes
- Estimate topic-level mastery
- Identify knowledge gaps

### 3. **Tutor Agent**
Acts as the student's personal instructor.

It dynamically changes its teaching strategy based on the learner profile:

```text
Beginner
 → Simple explanation
 → Analogy
 → Example
 → Guided practice

Intermediate
 → Concept explanation
 → Worked example
 → Application problem

Advanced
 → Deeper reasoning
 → Challenging problems
 → Exam-level questions
```

### 4. **Study Planner Agent**
Creates and continuously updates the study schedule.

The planner considers:

- Exam dates
- Available study hours
- Topic difficulty
- Topic importance
- Previous performance
- Revision requirements
- Unfinished lessons

When the student falls behind or improves faster than expected, the agent can **re-plan the remaining study schedule**.

### 5. **Quiz Agent**
Generates personalized quizzes rather than repeating a fixed question bank.

The agent can dynamically adjust:

- Difficulty
- Number of questions
- Topic distribution
- Question type
- Revision frequency

```text
Low mastery
    ↓
Easy → Medium → Practice

Improving
    ↓
Medium → Hard → Application

High mastery
    ↓
Hard → Exam-style → Revision
```

### 6. **Knowledge-Gap Agent**
Analyzes incorrect answers to determine **why** the student made a mistake.

Instead of simply recording:

```text
Question: Wrong
```

the system attempts to determine:

```text
Concept not understood
      OR
Calculation mistake
      OR
Misread question
      OR
Forgot formula
      OR
Confused related concepts
```

This allows the tutor to recommend the correct remediation.

### 7. **Revision Agent**
Automatically identifies topics that need revision.

The agent prioritizes concepts using:

```text
Weakness
×
Importance
×
Time since last revision
×
Exam proximity
```

This creates a continuously changing **revision queue**.

### 8. **Resource Recommendation Agent**
Connects the student's weaknesses with suitable learning resources such as:

- Notes
- Summaries
- Examples
- Practice questions
- Flashcards
- Previous questions
- Concept explanations

The system avoids giving the same resource to every student.

---

## Adaptive Learning Engine

The core of the system is an adaptive decision loop:

```text
Observe
   ↓
Assess
   ↓
Identify Knowledge Gap
   ↓
Plan
   ↓
Teach
   ↓
Practice
   ↓
Evaluate
   ↓
Update Student Model
   ↓
Re-plan
```

Every interaction can update the learner model, allowing the tutor to become more personalized over time.

## Personalization Model

Each topic maintains a dynamic mastery score.

```text
Topic
 ├── Mastery Score
 ├── Confidence Score
 ├── Accuracy
 ├── Attempts
 ├── Recent Performance
 ├── Mistake Patterns
 └── Revision Priority
```

Example:

```text
Data Structures

Arrays       → 92% mastery
Linked List  → 76% mastery
Stacks       → 61% mastery
Queues       → 84% mastery
Trees        → 43% mastery
Graphs       → 37% mastery
```

The tutor therefore spends more learning time on **Trees and Graphs** instead of repeatedly teaching Arrays.

## Adaptive Study Planning

The system automatically converts the student's academic goals into a learning plan.

```text
Goal
 ↓
Subjects
 ↓
Topics
 ↓
Priority Calculation
 ↓
Available Study Time
 ↓
Daily Schedule
 ↓
Practice + Revision
 ↓
Performance Feedback
 ↓
Schedule Adjustment
```

Example:

```text
Upcoming Exam: DBMS

High Priority
 → Normalization
 → Transactions
 → SQL

Medium Priority
 → Indexing
 → ER Model

Low Priority
 → Introduction
```

The priority changes automatically as the student's performance changes.

## Agentic Decision Making

The agents can work together to complete a learning objective.

Example:

```text
Student:
"I have an exam in 7 days and I'm weak in Operating Systems."

Planner Agent
        ↓
Breaks syllabus into topics

Assessment Agent
        ↓
Tests current knowledge

Knowledge-Gap Agent
        ↓
Finds weak concepts

Tutor Agent
        ↓
Explains weak concepts

Quiz Agent
        ↓
Creates targeted practice

Evaluation Agent
        ↓
Measures improvement

Planner Agent
        ↓
Updates the next day's schedule
```

This creates a **closed-loop autonomous learning system** instead of a question-answer chatbot.

## RAG / Knowledge Layer

The tutor can ground explanations and question generation using trusted academic material.

```text
Academic Documents
       ↓
Document Processing
       ↓
Chunking
       ↓
Embeddings
       ↓
Vector Database
       ↓
Semantic Retrieval
       ↓
Tutor / Quiz Agent
```

Possible knowledge sources include:

- Textbooks
- Lecture notes
- Syllabus documents
- PDFs
- Previous-year question papers
- Instructor-provided material

This helps the tutor generate answers relevant to the student's actual syllabus.

## Student Interaction

The tutor supports multiple learning modes:

```text
ASK
 ↓
Explain a concept

LEARN
 ↓
Follow a personalized lesson

PRACTICE
 ↓
Solve adaptive questions

TEST
 ↓
Attempt timed assessment

REVISE
 ↓
Review weak topics

PLAN
 ↓
Generate / update study schedule
```

## Dashboard

The student dashboard provides an overview of learning progress.

```text
┌─────────────────────────────────────┐
│          STUDY OVERVIEW             │
├─────────────────────────────────────┤
│ Overall Mastery          78%        │
│ Today's Progress         65%        │
│ Study Streak             12 days    │
│ Upcoming Exam            7 days     │
├─────────────────────────────────────┤
│ Strong Topics                        │
│  DBMS · SQL · Networks              │
├─────────────────────────────────────┤
│ Weak Topics                         │
│  OS Scheduling · Deadlocks          │
├─────────────────────────────────────┤
│ Today's Recommendation              │
│  Practice OS Scheduling — 35 min    │
└─────────────────────────────────────┘
```

## Key Features

- Personalized study plans
- Adaptive quizzes
- Topic-wise mastery tracking
- Automatic weak-area detection
- AI-generated explanations
- Automatic revision recommendations
- Exam-oriented preparation
- Progress analytics
- Study streak tracking
- Document-based tutoring
- Personalized question generation
- Continuous learner profiling
- Multi-agent orchestration
- Dynamic study-plan re-planning
- Context-aware tutoring

## Agentic AI Features

The major differentiator of the system is its ability to **take learning-related actions autonomously**.

```text
┌─────────────────────┐
│   Student Goal      │
└─────────┬───────────┘
          ↓
┌─────────────────────┐
│ Planner Agent       │
└─────────┬───────────┘
          ↓
┌─────────────────────┐
│ Assessment Agent    │
└─────────┬───────────┘
          ↓
┌─────────────────────┐
│ Knowledge-Gap Agent │
└─────────┬───────────┘
          ↓
┌─────────────────────┐
│ Tutor Agent         │
└─────────┬───────────┘
          ↓
┌─────────────────────┐
│ Quiz Agent          │
└─────────┬───────────┘
          ↓
┌─────────────────────┐
│ Evaluation Agent    │
└─────────┬───────────┘
          ↓
      Re-plan
```

The agent system can:

**Observe → Reason → Plan → Act → Evaluate → Adapt**

This enables the platform to function as a **proactive study companion** rather than a passive conversational assistant.

## Tech Stack

```text
Frontend
React / Next.js
TypeScript
Tailwind CSS

Backend
Python
FastAPI

AI / ML
PyTorch
Scikit-learn
LLM
Embeddings
RAG

Agentic Layer
Multi-Agent Orchestration
Tool Calling
Task Planning
Memory / Learner Profile

Data
PostgreSQL / SQLite
Vector Database

Document Processing
PDF Extraction
Text Chunking
Embedding Pipeline

Deployment
Docker
Streamlit / Web Application
```

## System Architecture

```text
                  ┌─────────────────────┐
                  │       Student       │
                  └──────────┬──────────┘
                             ↓
                  ┌─────────────────────┐
                  │   Web Application   │
                  └──────────┬──────────┘
                             ↓
                  ┌─────────────────────┐
                  │   Agent Orchestrator│
                  └──────────┬──────────┘
                             ↓
       ┌──────────────┬──────┴──────┬──────────────┐
       ↓              ↓             ↓              ↓
   Planner         Tutor        Assessment      Revision
    Agent          Agent           Agent          Agent
       │              │             │              │
       └──────────────┴──────┬──────┴──────────────┘
                             ↓
                  ┌─────────────────────┐
                  │ Learner Model / DB  │
                  └──────────┬──────────┘
                             ↓
                  ┌─────────────────────┐
                  │ Knowledge / RAG     │
                  │ Vector Database     │
                  └─────────────────────┘
```

## Quick Start

```bash
python -m venv .venv

# Windows
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

Configure the required environment variables:

```env
LLM_API_KEY=your_api_key
DATABASE_URL=your_database_url
VECTOR_DB_URL=your_vector_database_url
```

Start the backend:

```bash
.\.venv\Scripts\python.exe -m uvicorn backend.main:app --reload
```

Start the frontend:

```bash
npm install
npm run dev
```

## Example Workflow

```text
Student signs in
      ↓
Selects subject + exam date
      ↓
System generates diagnostic assessment
      ↓
Assessment Agent evaluates responses
      ↓
Knowledge-Gap Agent identifies weak concepts
      ↓
Planner Agent generates study schedule
      ↓
Tutor Agent teaches each concept
      ↓
Quiz Agent generates targeted practice
      ↓
Evaluation Agent measures improvement
      ↓
Learner model updated
      ↓
Planner automatically adjusts future sessions
```

## Repo Layout

```text
src/
 ├── agents/
 │    ├── planner_agent.py
 │    ├── tutor_agent.py
 │    ├── assessment_agent.py
 │    ├── quiz_agent.py
 │    ├── revision_agent.py
 │    └── knowledge_gap_agent.py
 │
 ├── ai/
 │    ├── llm.py
 │    ├── embeddings.py
 │    └── rag.py
 │
 ├── learner/
 │    ├── profile.py
 │    ├── mastery.py
 │    └── performance.py
 │
 ├── planner/
 │    └── adaptive_scheduler.py
 │
 ├── evaluation/
 │    └── evaluator.py
 │
 └── api/
      └── routes.py

app/
 ├── dashboard/
 ├── tutor/
 ├── quizzes/
 ├── planner/
 └── progress/

data/
 ├── syllabus/
 ├── notes/
 ├── question_bank/
 └── learner_data/

notebooks/
 └── experiments/

docs/
 ├── architecture.md
 ├── agent_workflow.md
 └── project_dossier.md
```

## Data Flow

```text
Student Interaction
        ↓
Interaction Logging
        ↓
Learner Model Update
        ↓
Mastery Estimation
        ↓
Agent Decision
        ↓
Personalized Action
        ↓
Student Response
        ↓
Feedback Loop
```

## Why Adaptive Study Tutor?

Traditional learning platforms generally provide the same content, questions, and learning sequence to every student.

This system changes that model:

```text
Traditional LMS
Student → Content → Quiz → Score

Adaptive Study Tutor
Student
  ↓
Observe
  ↓
Understand
  ↓
Plan
  ↓
Teach
  ↓
Practice
  ↓
Evaluate
  ↓
Adapt
  ↓
Teach Again
```

The objective is to create a **continuous personalized learning loop** where the system adapts to the learner instead of forcing the learner to adapt to a fixed course structure.

## Future Extensions

```text
Voice-based Tutor
        ↓
Multilingual Learning
        ↓
Handwritten Answer Evaluation
        ↓
Exam Performance Prediction
        ↓
Collaborative Learning Agents
        ↓
University LMS Integration
        ↓
Personalized Long-Term Learning Memory
```

## Tech Stack Summary

**React · Next.js · TypeScript · Tailwind CSS · Python · FastAPI · PyTorch · LLM · RAG · Vector Database · PostgreSQL · Multi-Agent AI · Tool Calling · Docker**
