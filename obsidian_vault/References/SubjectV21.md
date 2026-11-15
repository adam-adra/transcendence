# 42 ft_transcendence (Version 21.1) Subject Summary

> Comprehensive breakdown of mandatory requirements, modules, point matrix, and evaluation rules.

#reference #subject

## 1. General Constraints & Mandatory Rules
- **Stack Requirement**: Frontend + Backend + Database.
- **Containerization**: Single-command startup (e.g. `docker compose up --build`).
- **Browser Compatibility**: Latest Google Chrome. Zero warnings, zero errors in browser console.
- **Security & Network**: All browser-to-backend traffic MUST be **HTTPS** (e.g., Nginx SSL reverse proxy).
- **Multi-user Support**: Multiple simultaneous users, concurrent actions handled properly, no race conditions, real-time sync.
- **Auth & Validation**: Email & password authentication (passwords securely hashed and salted). Full input validation on both frontend AND backend. Local `.env` ignored by git, with `.env.example` in repo.
- **Styling**: Must use a CSS framework or styling solution (Tailwind CSS, Bootstrap, etc.).
- **Legal Requirements**: Privacy Policy and Terms of Service pages (accessible via footer links, realistic content, not empty/placeholders).
- **Git Hygiene**: Clean commit history from ALL team members with clear messages and equal distribution.
- **README.md Requirements**: Strict required structure, italicized first line with logins, team roles (PO, PM, Tech Lead, Developers), project management, tech stack, DB schema, features list, module point calculation, individual contributions.

## 2. Modules & Points System (Target: 14+ points)
- Major module = 2 points
- Minor module = 1 point
- Recommended target: 14 to 16 points (with safety buffer).

### Recommended Minimalist Module Selection ("The Golden Path"):
1. **Web (Major - 2 pts)**: Framework for frontend & backend (e.g. React/Vue + Django/FastAPI/NestJS/Fastify).
2. **Web (Major - 2 pts)**: Real-time features with WebSockets (graceful connection/disconnection, message broadcasting).
3. **Web (Minor - 1 pt)**: ORM for database (e.g. Prisma / Django ORM / TypeORM).
4. **User Management (Major - 2 pts)**: Standard user management & auth (profile updates, avatar upload with default, friend list & online status).
5. **User Management (Minor - 1 pt)**: OAuth 2.0 (42 Intra login).
6. **Gaming & UX (Major - 2 pts)**: Web-based game (Real-time Pong, 2D).
7. **Gaming & UX (Major - 2 pts)**: Remote players (2 players over network, latency handling, reconnection logic).
8. **Gaming & UX (Minor - 1 pt)**: Tournament system (bracket system, matchups, registration).
9. **Gaming & UX (Minor - 1 pt)**: Game customization (paddle speed/size, ball speed, map skins/power-ups).
10. **Artificial Intelligence (Major - 2 pts)**: AI Opponent for Pong (human-like behavior, predictive/heuristic, able to win occasionally).

**Total Points = 15 points** (Covers all mandatory dependencies cleanly without over-engineering like ELK or blockchain).

## Related
- [[Roadmap/BirdsEyeView]]
- [[Roadmap/Milestones]]
