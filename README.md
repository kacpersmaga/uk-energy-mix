# UK Energy Mix

Full-stack app built on the UK [Carbon Intensity API](https://carbon-intensity.github.io/api-definitions/): it shows the 3-day electricity generation mix and finds the cleanest window to charge an EV.

**Live:** https://energy-mix-frontend-0ru0.onrender.com/

| Part | Stack | Directory |
| --- | --- | --- |
| Backend | .NET 10 Web API, xUnit + NSubstitute, Docker | [`backend/`](backend) |
| Frontend | React 19, TypeScript, Vite, Tailwind, Recharts, Vitest | [`frontend/`](frontend) |

## Features

- **Energy mix:** one pie chart per day (today, tomorrow, day after) with the clean energy share (biomass, nuclear, hydro, wind, solar).
- **EV charging planner:** pick 1–6 hours and get the window over the next two days with the highest average clean energy share.

## Running locally

```bash
# backend (http://localhost:5197)
cd backend && dotnet run --project EnergyAPI

# frontend (http://localhost:5173)
cd frontend && npm install && npm run dev
```

Tests: `dotnet test` in `backend/`, `npm test` in `frontend/`.

See each directory's README for the design decisions.
