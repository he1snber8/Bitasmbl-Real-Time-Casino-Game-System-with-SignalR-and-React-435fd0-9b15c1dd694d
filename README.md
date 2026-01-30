# Bitasmbl-Real-Time-Casino-Game-System-with-SignalR-and-React-435fd0-9b15c1dd694d

## Description
Minimal real-time casino platform with Auth, Wallet, Lobby, and Game1 services using SignalR for all player communication, plus a React frontend and Docker Compose deployment.

## Tech Stack
- ASP.NET Core
- Docker
- React
- SignalR

## Requirements
- Implement LobbyHub methods to create, join, approve, cancel tables and ensure all player actions go through SignalR only.
- After receiving winner info from Game1, Lobby should credit 95% of prize pool via Wallet and keep 5% margin.
- Game1Hub must randomly select a winner after delayTime seconds once two players have joined the table.
- React Lobby page should render a dynamic form for game rules based on games.json and create tables through LobbyHub.
- Use JWT token from AuthService when establishing SignalR connections to Lobby and Game1.

## Installation
bash
git clone https://github.com/he1snber8/Bitasmbl-Real-Time-Casino-Game-System-with-SignalR-and-React-435fd0-9b15c1dd694d.git
cd Bitasmbl-Real-Time-Casino-Game-System-with-SignalR-and-React-435fd0-9b15c1dd694d
docker compose build


## Usage
bash
docker compose up


## Implementation Steps
1. Define Auth, Wallet, Lobby, and Game1 services in ASP.NET Core with SignalR hubs.
2. Implement LobbyHub methods for create, join, approve, cancel using SignalR-only player actions.
3. Implement Game1Hub to start countdown after two players join and randomly select winner after delayTime.
4. On winner notification, have Lobby call Wallet to credit 95% of prize pool and retain 5% margin.
5. Implement React Lobby page to load games.json and render dynamic form for game rules.
6. Use the dynamic form to create tables via LobbyHub.
7. Obtain JWT from AuthService and attach it when establishing SignalR connections to Lobby and Game1.

## API Endpoints
- SignalR hubs for Lobby and Game1 with JWT-based connections.