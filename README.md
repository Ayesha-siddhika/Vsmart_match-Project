# vSmart Match – Gen AI Powered, Talent Focused

## Overview
vSmart Match is a GenAI-powered talent-focused platform built with the MERN stack. It integrates Langflow and LangSmith for intelligent resume parsing, certificate validation, scoring, and contextual skill analysis. The platform visualizes results using dashboards and radar charts to enable smarter, faster hiring decisions.

---

## Features
- Create and manage rich job descriptions
- Upload and parse resumes (PDFs)
- GenAI-powered skill extraction, certificate validation, and resume scoring
- Spider chart visualization using Chart.js
- Filter candidates by job description, score, and category
- Propose/reject candidates and export filtered results to CSV
- GenAI-based chatbot for HR assistance
- Dropbox integration for cloud resume storage
- JWT authentication and user profile management
- Langflow and LangSmith integration for contextual parsing, scoring, and traceable AI workflows

---

## Prerequisites
Before running the project, ensure you have the following installed or configured:

- Node.js (v18 or higher)
- npm (v8 or higher)
- Python (v3.9 or higher)
- Git
- MongoDB (local or Atlas)
- Dropbox Developer Token
- Langflow and LangSmith accounts with API keys

---

## Quick Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/vsmart-match.git
cd vsmart-match
2. Install Dependencies
Backend

bash
Copy
Edit
cd Backend
npm install
Frontend

bash
Copy
Edit
cd ../Frontend/vSmart_Match
npm install
3. Environment Configuration
Create a .env file in both the Backend and Frontend directories.

Backend .env

env
Copy
Edit
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
DROPBOX_ACCESS_TOKEN=your_dropbox_access_token
LANGFLOW_API_KEY=your_langflow_api_key
LANGFLOW_FLOW_ID=your_flow_id
PORT=5000

LANGSMITH_TRACING=true
LANGSMITH_ENDPOINT=https://api.smith.langchain.com
LANGSMITH_API_KEY=your_langsmith_api_key
LANGSMITH_PROJECT=vSmart_Match
4. Start the Application
Start Backend

bash
Copy
Edit
cd Backend
node server.js
Runs at: http://localhost:5000

Start Frontend

bash
Copy
Edit
cd Frontend/vSmart_Match
npm run dev
Runs at: http://localhost:3000

Database Setup
Sign up at MongoDB Atlas

Create a cluster and get your connection string

Replace MONGO_URI in your backend .env

Whitelist your IP address in MongoDB Atlas

AI Integration Setup
Langflow Setup
bash
Copy
Edit
pip install langflow
langflow run --host 0.0.0.0 --port 7860
Create your AI flow

Get the Flow ID

Add LANGFLOW_FLOW_ID in your .env

LangSmith Setup
Sign up at LangSmith

Create a new project

Get your API key and update the backend .env

Dropbox Integration Setup
Go to Dropbox App Console

Create a new app with Scoped access

Generate an access token

Add token to .env

Project Structure
pgsql
Copy
Edit
vSmart_Match/
├── Frontend/
│   ├── public/
│   ├── src/
│   │   ├── assets/
│   │   ├── pages/
│   │   │   ├── Home.jsx
│   │   │   ├── JobDesc.jsx
│   │   │   ├── Login.jsx
│   │   │   ├── ResumeScreen.jsx
│   │   │   ├── Proposed.jsx
│   │   │   ├── ProfilePage.jsx
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   ├── MainPage.jsx
│   │   └── ProtectedRoute.jsx
│   ├── package.json
│   └── .env
├── Backend/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── uploads/
│   ├── server.js
│   ├── package.json
│   └── .env


## Screenshots

###  Login & Signup Page  
![Login & Signup](https://drive.google.com/uc?export=view&id=1xqUbfckgEBJHgO6kD-mjg-Bx6tiVKGle)

### Home Page  
![Home Page](https://drive.google.com/uc?export=view&id=1qEHEv-7UmHuVOgahalSXVmfnuoZg3x0c)

###  HR ChatBot  
![HR ChatBot](https://drive.google.com/uc?export=view&id=1HfkXvb8gycidpdxGtfsCRHibbYa2dOqX)

### Job Description  
![Job Description](https://drive.google.com/uc?export=view&id=1fQb_srcfKOakdqc5dYc4jDShbuejX09V)

### Resume Screening Page  
![Resume Screening](https://drive.google.com/uc?export=view&id=1PQdOS1u78vKejuGyZ4NGkcMo_LVkQcIo)

### Spider Graph (Skill Visualization)  
![Spider Graph](https://drive.google.com/uc?export=view&id=1cUKMsrpSBAHv4-S4qBZn4G2SDKkzI7Ti)

###  Proposed Resumes Page  
![Proposed Resumes](https://drive.google.com/uc?export=view&id=19VmAGVV8an2Yl9QhKuaX9wDH4jayuHhF)

###  Exported CSV  
![Exported CSV](https://drive.google.com/uc?export=view&id=13soiS9WwdeR8v-gNRFBoXgO_wyGo3zan)

###  Profile Page  
![Profile Page](https://drive.google.com/uc?export=view&id=1GVD2NgAhvIIdAQzN19m-W119ysiBqAdK)

###  Resume Screening via Langflow RAG  
![Langflow RAG](https://drive.google.com/uc?export=view&id=1Y1SiKrp2ZrTxVMmdKyDoNWabIupI25pf)

###  GenAI Chatbot via Langflow  
![GenAI Chatbot](https://drive.google.com/uc?export=view&id=17TnQ9cphkKSLHi7gqAXe_zOMoEKJ9Amn)

###  LangSmith Trace + Monitor  
![LangSmith Trace](https://drive.google.com/uc?export=view&id=1vtQYKMXmCBraLZvJDO01GsHaFr0QNYPZ)



Future Enhancements
RAG Model Integration for Context-Aware Responses

AI Vector Database for Semantic Resume Search

Enhanced Security with Role-Based Access Control (RBAC)

Langfuse Integration for External Monitoring & Tracing

Deployment Plan
Component	Hosting Platform	Notes
Frontend (React)	Render	Free/low-tier Node environment
Backend (Express)	Render	Connected to MongoDB & Langflow
Langflow	Render or Self-hosted	Port 7860
LangSmith	Cloud SaaS	Used for tracing/debugging
Database (MongoDB Atlas)	Cloud	Shared/Free Tier DB
Resume Storage (Dropbox)	Cloud	Public links for resume access

Architecture Diagram


Team
Frontend Developer – React.js, UI/UX

Backend Developer – Node.js, Express.js, MongoDB

AI/ML Engineer – Langflow, LangSmith Integration                 |
