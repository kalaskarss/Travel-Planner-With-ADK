# 🌍 AI Travel Planner using Google ADK

An **AI-powered Travel Planning Assistant** built using **Google Agent Development Kit (ADK)**.

This project demonstrates how **Agentic AI systems can collaborate using multiple specialized agents** to generate travel recommendations such as destinations, accommodation, and activities.

The system uses a **central controller agent** that coordinates multiple agents to produce a complete travel plan for users.

---

# 🚀 Features

- 🤖 AI-powered travel assistant
- 🧠 Multi-agent architecture using **Google ADK**
- 🗺️ Destination recommendations
- 🏨 Accommodation suggestions
- 🎯 Activity planning
- ⚡ Powered by **Gemini LLM**

---

# 🧠 Architecture

root_agent (travel_planner_main)
		└─ travel_inspiration_agent
					├─ news_agent  (uses google_search_grounding tool)
					└─ places_agent (uses location_search_tool -> Overpass + Nominatim)

Tools:
	google_search_grounding -> wraps a search agent providing bullet-point grounded results
	location_search_tool    -> FunctionTool: find_nearby_places_open(query, location, radius, limit)

# <img width="2850" height="1677" alt="ai_travel_planner_architecture" src="https://github.com/user-attachments/assets/09d9e001-d35b-400d-9fa7-2a16672ee364" />



### Architecture Overview

The system follows a **multi-agent architecture** where a central controller coordinates multiple specialized agents.

**User Input**
- The user asks for travel recommendations.

**Travel Planner Controller (Main Agent)**
- Built using Google ADK
- Understands the user request
- Delegates tasks to specialized agents

**Agent Coordination Layer**
- Manages communication between agents
- Aggregates responses

**Specialized Agents**

1️⃣ **Places Agent**
- Suggests travel destinations
- Recommends tourist attractions

2️⃣ **Accommodation Agent**
- Suggests hotels and stays

3️⃣ **Activity Agent**
- Recommends activities and experiences

**LLM Model (Gemini)**
- Provides reasoning and response generation for agents.

---

# 🏗️ Tech Stack

- **Python**
- **Google Agent Development Kit (ADK)**
- **Gemini LLM**
- **Agentic AI Architecture**

---

# 📂 Project Structure

```
travel-planner-with-adk/
├── main.py
├── pyproject.toml
├── README.md
└── travel_planner/
		├── agent.py
		├── supporting_agents.py
		├── tools.py
		└── __pycache__/ (ignored)
```

---

# ▶️ Running the Project

Clone the repository:

```bash
git clone https://github.com/kalaskarss/Travel-Planner-With-ADK.git
cd travel-planner-with-adk
```

Run the application:

uv run python main.py
---

# 🎯 Purpose of the Project

This project demonstrates how **multi-agent AI systems can collaborate using Google ADK** to solve real-world problems such as travel planning.

It serves as a **learning project for Agentic AI and Google ADK** and can be used as a **portfolio project for AI/ML engineers**.

---

# 🔮 Future Improvements

- Flight recommendation integration
- Budget-based trip planning
- Weather API integration
- Interactive travel maps
- Personalized itineraries

