# Bird's Eye View

> The full system understood from above, before touching any code.

#architecture #roadmap

## What are we building?
A real-time multiplayer online Pong web application containerized with Docker, featuring user authentication (standard + OAuth), profiles, real-time matchmaking, tournaments, customizable game rules/skins, an AI opponent, and HTTPS encryption.

## Main components
- **Frontend SPA**: Client interface (HTML5 Canvas game view, auth forms, lobby/chat, tournament brackets, profiles).
- **Backend Server**: API handling auth, user accounts, game state machine via WebSockets, AI calculation, tournament coordination.
- **Database**: Persistent storage for users, match history, friendships, settings.
- **Nginx Gateway**: Handles TLS/HTTPS termination, static asset serving, and reverse proxying API and WebSockets.

## How they connect
```
Client Browser (Google Chrome / HTTPS)
       │
       ▼
 [ Nginx Reverse Proxy (SSL :443) ]
       │
       ├───► /api/*         ──► Backend API (REST) ──► Database (PostgreSQL)
       ├───► /ws/*          ──► Backend WebSocket (Game/Chat/State)
       └───► /*             ──► Frontend Static Assets (SPA)
```

## Key constraints
- Single command launch: `docker compose up --build`.
- Zero browser console errors or warnings.
- HTTPS everywhere externally.
- Multi-user concurrency without state desync.
- Must fulfill 14+ points from the v21.1 module catalog.

## Related
- [[Roadmap/Terminology]]
- [[Roadmap/Milestones]]
- [[References/SubjectV21]]
