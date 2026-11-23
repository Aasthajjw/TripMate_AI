# ✈️ TripMate AI – Multi-Agent Travel Planner

An AI-powered travel planning application built using **LangGraph, LangChain, Groq, and FastAPI**. TripMate AI uses a multi-agent architecture to simplify travel planning by coordinating specialized AI agents for flight research, hotel recommendations, and personalized itinerary generation.

## 🌍 Project Overview

Planning a trip involves researching flights, comparing hotels, creating itineraries, and organizing travel information. TripMate AI simplifies this process through an intelligent multi-agent system.

Users can enter their travel requirements, and the application coordinates multiple AI agents to generate a comprehensive travel plan.

## ✨ Key Features

- **AI-Powered Travel Planning:** Generates personalized travel plans based on user requirements.
- **Flight Research Agent:** Retrieves flight-related information using AviationStack.
- **Hotel Research Agent:** Uses Tavily search to research hotel options and accommodation information.
- **Itinerary Generation Agent:** Creates structured, day-wise travel itineraries.
- **Multi-Agent Coordination:** Uses LangGraph to manage communication and workflow between specialized agents.
- **AI-Powered Responses:** Uses Groq LLMs for intelligent reasoning and natural-language generation.
- **Interactive Web Interface:** Provides a user-friendly interface for submitting travel requests and viewing generated plans.
- **Conversation Persistence:** Uses PostgreSQL for storing LangGraph conversation checkpoints.

## 🏗️ System Architecture

TripMate AI follows a multi-agent architecture where each agent performs a specialized task.

```text
             USER INPUT
                  |
                  v
          FASTAPI BACKEND
                  |
                  v
          LANGGRAPH WORKFLOW
                  |
       +----------+----------+
       |          |          |
       v          v          v
   FLIGHT       HOTEL     ITINERARY
   AGENT        AGENT       AGENT
       |          |          |
       v          v          v
  AviationStack Tavily    Groq LLM
       |          |          |
       +----------+----------+
                  |
                  v
         FINAL RESPONSE AGENT
                  |
                  v
          COMPLETE TRAVEL PLAN
```

### AI Agents

| Agent | Responsibility |
|---|---|
| Flight Agent | Retrieves flight-related information |
| Hotel Agent | Researches hotels and accommodation |
| Itinerary Agent | Generates personalized travel itineraries |
| Final Response Agent | Combines agent outputs into a structured response |

## 🛠️ Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Backend | FastAPI |
| AI Orchestration | LangGraph |
| LLM Framework | LangChain |
| Language Model | Groq |
| Web Search | Tavily API |
| Flight Information | AviationStack API |
| Database | PostgreSQL |
| Frontend | HTML, CSS, JavaScript |
| Version Control | Git & GitHub |

## 📁 Project Structure

```text
TripMate-AI/
│
├── app.py
├── backend.py
├── requirements.txt
├── .env
├── .gitignore
│
├── static/
│   ├── style.css
│   └── script.js
│
├── templates/
│   └── index.html
│
└── README.md
```

*Note: The structure above illustrates the main application files. Additional project files and folders may be present.*

## ⚙️ Installation and Setup

Follow these steps to run TripMate AI locally.

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/TripMate-AI.git
```

Navigate to the project directory:

```bash
cd TripMate-AI
```

### 2. Create a Virtual Environment

```bash
python -m venv .venv
```

Activate it on Windows:

```powershell
.venv\Scripts\Activate.ps1
```

### 3. Install Dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
pip install certifi
```

### 4. Configure Environment Variables

Create a `.env` file in the root directory and add the following credentials:

```env
GROQ_API_KEY=your_groq_api_key

TAVILY_API_KEY=your_tavily_api_key

AVIATIONSTACK_API_KEY=your_aviationstack_api_key

DATABASE_URL=your_postgresql_database_url

DEFAULT_ORIGIN_IATA=CCU
```

Replace the placeholders with your actual API keys and database connection URL.

### 5. Run the Application

Start the FastAPI application:

```bash
python app.py
```

Open your browser and navigate to:

```text
http://127.0.0.1:8000
```

The application should now be accessible locally.

## 🔑 Required API Services

The project integrates the following external services:

| Service | Purpose | Official Website |
|---|---|---|
| Groq | LLM inference and AI responses | https://console.groq.com/ |
| Tavily | Web search and hotel research | https://app.tavily.com/ |
| AviationStack | Flight information | https://aviationstack.com/ |
| Render PostgreSQL | Persistent database | https://render.com/ |

**Important:** API keys and database credentials must be kept private. Never commit your `.env` file to GitHub.

## 🗄️ Database

TripMate AI uses PostgreSQL to persist LangGraph conversation checkpoints.

Configure the `DATABASE_URL` environment variable with a valid PostgreSQL connection string before starting the application.

## ⚠️ Important Notes

- An active internet connection is required for external API integrations.
- API usage is subject to the respective provider's rate limits and subscription plans.
- AviationStack provides flight-related information; it does not independently guarantee real-time ticket prices or booking availability.
- AI-generated itineraries and recommendations should be verified before making actual travel arrangements.
- The application requires valid API credentials and a working PostgreSQL connection.

## 🚀 Future Enhancements

Potential improvements include:

- Integration with additional flight and hotel booking APIs.
- Real-time flight fare comparison.
- Interactive maps and location-based recommendations.
- Personalized travel budgets and expense tracking.
- User authentication and profile management.
- PDF export of generated itineraries.
- Weather-based travel recommendations.
- Deployment with scalable cloud infrastructure.

## 👩‍💻 Author

**Aastha Jhunjhunwala**

B.Tech (Hons.) – Aerospace Engineering

Interested in Artificial Intelligence, Machine Learning, and Multi-Agent Systems.

## 📄 License

This project is intended for educational and development purposes. Refer to the original repository's license and attribution requirements before redistributing or modifying its code.

---

⭐ If you find this project interesting, consider starring the repository!