1. **Semantic Understanding:** The LLM processes conversational inputs (e.g., *"A 3-day budget-friendly hidden culinary tour of Kyoto"*) rather than rigid criteria.
2. **Data Grounding & Retrieval:** The agents extract live geographic data, reviews, and dynamic pricing parameters using multi-source APIs.
3. **Algorithmic Validation:** A hard constraint-checking layer reviews opening times, travel windows, and physical distance matrix elements before generating payloads.
4. **State Serialization:** Data maps directly into strongly typed schemas, feeding the split-screen UI via WebSockets for real-time multiplayer coordination.

---

## 🛠️ Unified Repository Blueprint

```text
ai-trip-planner/
├── backend/                  # FastAPI Core, LangGraph Workflows, & Vector DB Layer
│   ├── app/
│   │   ├── api/              # API Routers & Endpoints (v1)
│   │   ├── core/             # Pydantic Settings & Security Configurations
│   │   ├── db/               # SQLAlchemy Session Engine & pgvector Utilities
│   │   ├── models/           # Relational Database Models (PostgreSQL)
│   │   ├── schemas/          # Data Validation & Serialization Layers (Pydantic)
│   │   ├── services/         # Third-Party API Service Clients
│   │   └── agents/           # LangGraph Workflows, Node Definitions, & States
│   ├── alembic/              # Relational Database Schema Migrations
│   └── requirements.txt      # Python Microservices Manifest
│
├── frontend/                 # Vite + React Client Application
│   ├── src/
│   │   ├── assets/           # Dynamic style manifests, branding assets
│   │   ├── components/       # Presentational UI Blocks & Global Map Wrapper
│   │   ├── features/         # Domain-Driven State Core (Planner, Auth, Dashboard)
│   │   ├── hooks/            # Encapsulated state lifecycles (useMapbox, useAuth)
│   │   ├── services/         # Network client engine layer (Axios interceptors)
│   │   └── context/          # Shared State Engine (Real-time Timeline/Map coordination)
│   └── package.json          # Node.js Module Dependency Manifest
│
└── README.md                 # Project Orchestration Guide
```

🚀 Quickstart Development Environment Setup Prerequisites
- Python 3.11+ installed globally.

- Node.js v20+ (LTS) environment.

- Docker & Docker Compose for container orchestration (Database layer).

Step 1: Clone the Repository

```bash
git clone [https://github.com/your-username/ai-trip-planner.git](https://github.com/your-username/ai-trip-planner.git)
cd ai-trip-planner
```
Step 2: Initialize Core Services Stack
Spin up pre-configured PostgreSQL enhanced with pgvector extensions using the root infrastructure config:

```bash
docker compose up -d
```

Step 3: Run Sub-System Environments
Follow the individual runtime guides inside the operational subdirectories:

#### Backend Microservice Portal: Go to Backend Setup

#### Frontend Portal Dashboard: Go to Frontend Setup

### 🌌 Modern 2026 Core Features
Neuro-Symbolic Pipeline: 
Merges flexible generative intelligence with rigid, rule-based algorithmic verification loops to permanently eliminate trip hallucination vectors.

Bi-Directional Context Engine: State modifications on the graphical drag-and-drop chronological timeline are immediately mapped as dynamic vectors over the active map topology.

Semantic Discovery Engine: Utilizes Vector Embeddings (pgvector) to discover local locations based entirely on conceptual descriptions ("cozy dark-academia reading spots") instead of exact categorical queries.

Real-time Collaboration Framework: Integrated WebSocket loops maintain multi-user operations across unified planning viewspaces simultaneously.