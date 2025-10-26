# Inorganic Waste & Scrap Management — Local Development

This repository contains a MERN-style monorepo with `backend/` (Express + MongoDB) and `frontend/` (Vite + React).

Quick start (recommended: use two terminals)

1. Install dependencies (once):

```powershell
# from repo root
npm install
npm --prefix .\backend install
npm --prefix .\frontend install
```

2. Start servers (open two PowerShell terminals):

Terminal A (backend):

```powershell
cd .\backend
npm run dev
# nodemon will run the backend on http://localhost:5000
```

Terminal B (frontend):

```powershell
cd .\frontend
npm run dev
# Vite will run the frontend on http://localhost:5173
```

3. Seed the database (optional, creates sample users and data):

```powershell
npm --prefix .\backend run seed
```

4. Use the app:

- Frontend: http://localhost:5173
- Backend: http://localhost:5000

Seeded test users:

- admin@example.com / password123
- citizen1@example.com / password123

Notes

- The root `npm run dev` script uses `concurrently`; PowerShell may prompt `Terminate batch job (Y/N)?` when running long-lived processes from some contexts. For a stable interactive session prefer running backend and frontend in separate terminals as shown above.
- If you prefer a single command, `npm run dev` at the repo root will attempt to start both services using `concurrently`.
