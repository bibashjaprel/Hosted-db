# Hosted-db

Small workspace containing Docker Compose setups for local databases used in development.

- [PostgreSQL](./pgs-db)
- [MySQL](./mysql-db)
- [MS SQL Server](./mssql-db)

## How To Setup any Database
0. Ensure you have Docker and Docker Compose    installed on your machine.
1. Navigate to the respective database folder.
# Hosted-db

Small workspace with Docker Compose setups for local development databases.

Quick links
- [PostgreSQL](./pgs-db)
- [MySQL](./mysql-db)
- [MS SQL Server](./mssql-db)

Prerequisites
- Docker (Desktop or Engine)
- Docker Compose

Getting started (PowerShell)

1. Open PowerShell/Terminal and change to the service folder, for example:

    cd .\mssql-db

2. Start the service in detached mode:

    docker-compose up -d

3. Stop and remove containers:

    docker-compose down

Environment and connection
- Each service folder contains a `docker-compose.yml` and may include a `.env` with connection details.
- Use the exposed ports and environment variables to connect with your client or application.

Ignoring local tool files

This repository includes a `.gitignore` at the root. The `.system/` folder is intentionally ignored to keep local tooling files out of source control.

If `.system` was already committed, stop tracking it while keeping files locally:

    git add .gitignore
    git commit -m "Add .system/ to .gitignore"
    git rm -r --cached .system
    git commit -m "Stop tracking .system and honor .gitignore"
    git status --ignored
    git check-ignore -v -- .system

Notes
- Replace `mssql-db` with `mysql-db` or `pgs-db` to manage the other database services.
- If you need seed data for MS SQL, look in `mssql-db/data` (or the top-level `mssql-db/data/` in this repo).
