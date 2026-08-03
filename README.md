✈️ Rover AI — Multi-Agent Travel Planner

Rover AI is an end-to-end AI travel planning assistant that turns a single natural-language request — like "Plan a 7-day Japan trip from India under a budget" — into a complete itinerary with flight info, hotel suggestions, and a day-by-day plan.

It's built using a multi-agent architecture powered by LangGraph, where specialized agents handle flights, hotels, and itinerary generation independently, then combine their results into a single response.

🚀 Features
Natural language trip planning — no forms, just describe your trip
Multi-agent orchestration using LangGraph (flight agent, hotel agent, itinerary agent, response formatter)
Real-time flight data via the AviationStack API
Hotel & travel research via the Tavily search API
Fast LLM inference using Groq
Persistent conversation memory — remembers context across sessions using PostgreSQL checkpointing
Clean web interface to interact with the planner directly in the browser
PDF export of your generated travel plan
🧠 How It Works
You submit a trip request through the web interface.
A Flight Agent searches for relevant flight data.
A Hotel Agent searches the web for hotel options.
An Itinerary Agent uses an LLM to build a day-by-day travel plan from the gathered data.
A Formatter Agent combines everything into a single, clean response.
The conversation is saved to PostgreSQL, so context carries over if you continue chatting.

LangGraph manages the flow between agents — similar to a manager routing tasks between specialized team members, rather than one model trying to do everything at once.

🛠️ Tech Stack
Layer	Technology
Backend	FastAPI
Agent Orchestration	LangGraph
LLM Inference	Groq
Database / Memory	PostgreSQL
Flight Data	AviationStack API
Hotel / Web Search	Tavily API
Frontend	HTML, CSS, JavaScript (Jinja2 templates)
Environment	Python 3.11+

You can get free-tier API keys from:

Groq Console
Tavily
AviationStack

.

📁 Project Structure
rover-ai/
├── app.py                 # FastAPI application entry point
├── backend.py              # LangGraph agent orchestration logic
├── Tools/
│   ├── tavily_tool.py       # Hotel/web search tool
│   └── flight_tool.py       # Flight search tool
├── static/
│   ├── style.css             # Frontend styling
│   └── script.js             # Frontend logic
├── templates/
│   └── index.html            # Main web page
├── requirements.txt
├── .env                     # API keys (not committed)
└── README.md
Neon or Supabase for a free PostgreSQL database

🖥️ Usage
Open the web app in your browser.
Type a travel request, e.g.:

"Plan a complete 7-day Japan trip from India including flights, hotels, and sightseeing under a budget."

Click Generate Plan.
View your itinerary, copy it, or download it as a PDF.
🌱 Future Improvements
Add support for multi-city trips
Add user authentication for saved trip history
Integrate real-time pricing (not just live flight status)
Add a map view for the itinerary
📄 License

This project is open source and available under the MIT License.
