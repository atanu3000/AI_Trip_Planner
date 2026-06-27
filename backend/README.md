# ⚙️ HorizonAI Core Backend Engine

This directory houses the foundational high-performance API microservice running **FastAPI**. It controls the intelligent workflow graphs, vectors data indices, database structures, and internal algorithmic optimization logic.

---

## 🛠️ Technical Stack Profile

* **Engine Core:** FastAPI (High-performance, fully asynchronous Python structural blueprint).
* **Agent Flow Pipeline:** LangGraph / LangChain (State-aware, loop-supported multi-agent systems orchestration framework).
* **LLM Engine Integration:** Gemini 2.0 Flash / GPT-4o-mini (Native structured JSON operational responses).
* **Data Storage Engines:** PostgreSQL + `pgvector` (Combined structured tables and high-velocity vector search arrays).
* **ORM:** SQLAlchemy + Alembic (Database connectivity mapping and sequential migration tools).

---

## 📂 Internal Directory Architecture

```text
backend/
├── app/
│   ├── api/                  # API Sub-routes
│   │   ├── endpoints/        # Endpoints for (auth.py, trips.py, ai.py)
│   │   └── router.py         # Primary master router mapping
│   ├── core/                 # Secure app configurations and system secrets
│   ├── db/                   # Database engines and raw vector indexing configs
│   ├── models/               # SQLAlchemy core relational models
│   ├── schemas/              # Pydantic schemas validating inputs and responses
│   ├── services/             # Dynamic HTTP clients (Google Maps, Amadeus, Weather)
│   └── agents/               # LangGraph state nodes, graphs, and tool actions
│       ├── graph.py          # State structural workflow map
│       ├── state.py          # State parameters and interfaces
│       └── nodes/            # Separate agent scripts (researcher, router, validator)
├── alembic/                  # Relational database schema generation records
├── requirements.txt          # Python environments manifest
└── .env.example              # Template containing system variables configurations
```

### 🚀 Environment Initialization Pipeline
1. Set Up a Virtual Environment
```Bash
cd backend
python3 -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```
2. Install Required Dependencies
```Bash
pip install -r requirements.txt
```
3. Establish Runtime Environment Configuration
Create a .env configuration template file inside the project directory root:

```text
DATABASE_URL=postgresql+asyncpg://postgres:postgres@localhost:5432/horizonai
JWT_SECRET_KEY=generate_a_secure_hexadecimal_string
GEMINI_API_KEY=your_gemini_api_key
GOOGLE_MAPS_API_KEY=your_google_maps_key
AMADEUS_API_KEY=your_amadeus_key
OPENWEATHER_API_KEY=your_weather_key
```
4. Execute Relational Schema Migrations
```Bash
alembic upgrade head
```
5. Launch the Uvicorn Asynchronous Web Server
```Bash
uvicorn app.main:app --reload
```
The localized interactive API documentation interface will instantly mount at: http://127.0.0.1:8000/docs.