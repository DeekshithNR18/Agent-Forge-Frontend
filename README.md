# AGENTVERSE – Frontend

AGENTVERSE is a web-based interface for an AI-powered application-building platform. The idea is to take a user's project requirements and organize the development process through a team of specialized AI agents.

Instead of handling every development task with a single AI assistant, AGENTVERSE is designed around multiple agents, each with a specific responsibility, from planning and coding to testing and deployment.

This repository contains the frontend of the project. It provides the interface where users can enter their ideas, select the type of application they want to build, and explore the agent workflow.

## Features

- **Interactive workspace:** A dedicated interface for working with AGENTVERSE.
- **Project input:** Enter an idea and choose the type of application you want to create.
- **Multi-agent workflow:** Displays six specialist agents and their responsibilities.
- **Agent selection:** Explore each agent and understand its role in the development process.
- **Login and signup screens:** Frontend interfaces for user access.
- **Light and dark themes:** Switch between different visual themes.
- **File input interface:** Supports selecting files through the frontend.
- **Responsive styling:** A custom interface designed for a modern web experience.

## The AI Agents

AGENTVERSE is organized around six agents:

| Agent | Responsibility |
|---|---|
| Orchestrator | Coordinates the overall workflow and assigns tasks. |
| Planner | Breaks the project idea into architecture and development tasks. |
| Builder | Handles application implementation. |
| Tester | Checks the application and identifies issues. |
| Fixer | Helps address failures and suggests corrections. |
| Deployer | Prepares the application for release and delivery. |

The frontend represents these roles visually. Their actual AI operations depend on integration with the backend and agent system.

## Tech Stack

- **React** – Building the user interface and managing application state.
- **Vite** – Development server and production build tooling.
- **JavaScript (ES modules)** – Application logic.
- **CSS** – Layout, styling, animations and themes.
- **Supabase JavaScript client** – Available for backend services and authentication integration.

## Project Structure

```text
agentverse_frontend/
├── src/
│   ├── lib/
│   │   └── supabase.js
│   ├── App.jsx
│   ├── App.css
│   ├── index.css
│   └── main.jsx
├── .env.example
├── index.html
├── package.json
└── README.md
```

## Getting Started

Follow these steps to run the frontend on your local machine.

### Prerequisites

Install the following:

- [Node.js](https://nodejs.org/) (a version compatible with the installed Vite version)
- npm, which comes with Node.js
- [Visual Studio Code](https://code.visualstudio.com/) or another code editor

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Replace `YOUR_GITHUB_REPOSITORY_URL` with your actual GitHub repository URL.

### 2. Open the project folder

```bash
cd agentverse_frontend
```

If you cloned the repository under a different folder name, use that folder name instead.

### 3. Install dependencies

```bash
npm install
```

This installs the packages listed in `package.json`.

### 4. Configure environment variables

Create a `.env` file in the project root using `.env.example` as a reference.

```env
VITE_SUPABASE_URL=YOUR_SUPABASE_PROJECT_URL
VITE_SUPABASE_PUBLISHABLE_KEY=YOUR_SUPABASE_PUBLISHABLE_KEY
VITE_API_BASE_URL=http://127.0.0.1:8000
```

Fill in the Supabase values if you are using Supabase. Keep the API URL aligned with the address where your backend is running.

Do not commit private credentials, service-role keys or other server secrets to GitHub.

### 5. Start the development server

```bash
npm run dev
```

Open the local URL printed in the terminal, usually:

```text
http://localhost:5173
```

### 6. Build for production

To check whether the frontend can be built for production, run:

```bash
npm run build
```

To preview the production build locally:

```bash
npm run preview
```

## Backend Integration

The frontend is intended to work with a separate backend that manages project creation and the AI-agent workflow.

The planned API integration uses these endpoints:

| Method | Endpoint | Purpose |
|---|---|---|
| POST | `/projects` | Create a project. |
| POST | `/projects/{project_id}/plan` | Request project planning. |
| POST | `/projects/{project_id}/run` | Start the project workflow. |
| GET | `/projects/{project_id}` | Retrieve project information and status. |

The expected local backend URL is:

```text
http://127.0.0.1:8000
```

These endpoints need to be implemented and connected to the frontend before the complete workflow can operate through the real backend.

## Current Development Status

The frontend includes the main interface, project input screens, agent workspace and a simulated workflow for demonstrating the user experience.

The next integration steps are to connect project creation to the backend, send user requirements to the agent system, display actual agent progress, and show the generated application's results.

Supabase configuration is also provided for integration, but real authentication and persistent user data should be verified separately.

## Future Improvements

- Connect the frontend to the working backend APIs.
- Stream live agent updates into the workspace.
- Display generated source code and application previews.
- Add project history and persistent storage.
- Integrate real testing, error recovery and deployment results.
- Improve error handling for failed API requests.

## Contributing

This project is being developed as a team project. Changes and improvements to the frontend can be made through feature branches and pull requests.

## License

No license has been specified yet. Add a license file if you plan to distribute or reuse this project publicly.

---

Built as part of the AGENTVERSE project, with the goal of making AI-assisted application development more organized and easier to follow.
