# ✈️ Rover AI

### AI-Powered Multi-Agent Travel Planning System

Rover AI is an AI-powered travel planning application that uses a **multi-agent architecture** to transform a user's travel requirements into a structured and personalized trip plan.

Instead of relying on a single AI agent, the application divides the planning process into specialized tasks such as **flight research, accommodation discovery, itinerary generation, and response preparation**. These agents work together through a **LangGraph-based workflow** to produce a complete travel plan from a simple natural-language request.

---

## 🚀 Key Features

* 🤖 **Multi-Agent Travel Planning** — Different agents handle different parts of the planning process.
* ✈️ **Flight Research** — Retrieves flight-related information based on the user's travel requirements.
* 🏨 **Hotel & Accommodation Research** — Uses web search to find suitable accommodation options.
* 🗺️ **Personalized Itinerary** — Generates a structured day-by-day travel schedule.
* 🧠 **LangGraph Workflow** — Coordinates communication and execution between the agents.
* 💬 **Natural Language Interaction** — Users can describe their trip requirements conversationally.
* ⚡ **LLM-Powered Responses** — Uses an LLM to reason over collected information and generate the final response.
* 🌐 **Web Interface** — Provides a simple interface for interacting with the travel planner.
* 💾 **Conversation State** — Maintains relevant travel-planning state throughout the workflow.

---

## 🧠 How It Works

The system follows a sequential multi-agent workflow:

```text
                 User Request
                      │
                      ▼
              ┌───────────────┐
              │  Travel Input │
              └───────┬───────┘
                      │
                      ▼
             ┌──────────────────┐
             │  Flight Agent    │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │   Hotel Agent    │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │ Itinerary Agent  │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │ Response Agent   │
             └────────┬─────────┘
                      │
                      ▼
              Final Travel Plan
```

### Workflow

1. The user provides their destination, duration, budget, and other travel preferences.
2. The **Flight Agent** gathers relevant flight information.
3. The **Hotel Agent** researches accommodation options.
4. The **Itinerary Agent** organizes the collected information into a practical travel schedule.
5. The **Response Agent** combines the results into a clear final travel plan.
6. The completed plan is returned to the user through the web application.

---

## 🛠️ Technologies Used

| Technology                  | Purpose                            |
| --------------------------- | ---------------------------------- |
| **Python**                  | Core application development       |
| **LangGraph**               | Multi-agent workflow orchestration |
| **LangChain**               | LLM and tool integration           |
| **Groq**                    | LLM inference                      |
| **FastAPI**                 | Backend API                        |
| **PostgreSQL**              | Conversation/state persistence     |
| **Tavily**                  | Web-based travel research          |
| **AviationStack**           | Flight information                 |
| **HTML / CSS / JavaScript** | Frontend interface                 |



## 🔑 Environment Variables

Create a `.env` file in the project directory and add the required API credentials:

```env
DATABASE_URL=your_postgresql_connection_string

GROQ_API_KEY=your_groq_api_key

TAVILY_API_KEY=your_tavily_api_key

AVIATIONSTACK_API_KEY=your_aviationstack_api_key

DEFAULT_ORIGIN_IATA=your_origin_airport_code
```

> **Important:** Never commit your `.env` file or expose API keys publicly.


## 💡 Example

A user can provide a request such as:

```text
Plan a 5-day trip to Tokyo with a budget of $1500.
Include flight options, hotels and a day-by-day itinerary.
```

The system processes the request through the different agents and returns a consolidated travel plan.

---

## 🎯 Project Objective

The main objective of this project was to explore how **multiple specialized AI agents can collaborate on a real-world problem**.

Rather than asking one LLM to perform every task, the application separates responsibilities into individual agents and uses **LangGraph to coordinate the overall workflow**.

This architecture makes the system easier to extend with additional capabilities such as:

* 🌤️ Weather information
* 🍽️ Restaurant recommendations
* 🚗 Transportation planning
* 💰 Budget optimization
* 🎟️ Activity and attraction discovery

---

## 🔮 Future Improvements

* Add weather-based recommendations
* Add restaurant and activity planning
* Improve budget tracking
* Add user authentication
* Add map-based destination visualization
* Introduce additional specialized agents
* Add human-in-the-loop approval for travel decisions
* Deploy the application as a cloud service

---

## 📌 Learning Outcomes

Through this project, I explored:

* Multi-agent AI architectures
* LangGraph state-based workflows
* LLM and tool integration
* API-based information retrieval
* Prompt design for specialized agents
* Backend development with FastAPI
* PostgreSQL-based state management
* Building an end-to-end AI application

---

## 👨‍💻 Project

**Rover AI — Multi-Agent Travel Planner**

Built as a hands-on project to explore **Agentic AI, LangGraph, LangChain, and LLM-powered applications**.

