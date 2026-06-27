## 📂 Internal Directory Architecture

```text
frontend/
├── src/
│   ├── assets/               # Local dynamic visuals, style matrices, branding assets
│   ├── components/           # Generic presentational layouts
│   │   ├── common/           # Atomic components (Buttons, Modals, Forms)
│   │   └── map/              # Vector map views, custom markers, route mapping lines
│   ├── features/             # Domain-focused operational units
│   │   ├── auth/             # Login/registration workflows
│   │   ├── dashboard/        # Itinerary listing viewspaces
│   │   └── planner/          # Full split-screen trip builder workspace
│   │       ├── Timeline.jsx  # Context-locked chronological scheduling sheet
│   │       └── Budget.jsx    # Real-time expense categorization matrix
│   ├── hooks/                # Specialized custom state hooks (useMapbox, useAuth)
│   ├── services/             # Base API network clients configuration (Axios)
│   └── context/              # Central synchronized state (TripContext)
├── package.json              # Client dependencies manifest
└── .env.example              # Variables template containing mapping public tokens
```

🚀 Environment Initialization Pipeline
1. Change Directory to Frontend Root
```Bash
cd frontend
```
2. Install Dependencies
```Bash
npm install
```
3. Setup Client Environment Variables
Create a local .env setup mapping keys within the client environment root:

```text
VITE_API_BASE_URL=http://localhost:8000/api/v1
VITE_MAPBOX_PUBLIC_TOKEN=your_mapbox_public_token_here
```
4. Launch the Local Development Server
```Bash
npm run dev
```
The user application client portal layer will immediately serve traffic live at: `http://localhost:5173`.