# Architecture Decision Record

## System Design Overview
The platform follows a modular monolith architecture designed for reliability, simplicity, and ease of self-hosting via Docker[cite: 11, 12]. 

## Key Technical Decisions
1. **Containerization (Docker):** Chosen to guarantee that the application runs locally without depending on external cloud services, hosted databases, or network connectivity[cite: 11, 12].
2. **Role Isolation:** Enforced at the middleware level to clearly separate permissions between Participants, Judges, Organizers, and Admins[cite: 10].
3. **Database Layer:** Utilizes a lightweight relational database via Docker to manage relational entities like users, teams, events, and project submissions cleanly.
