# Dockset Local

This repository contains ready-to-use Docker Compose setups for common development services. Use these to quickly spin up databases and tools for your projects.

## Available Stacks

- **MySQL**: `mysql/docker-compose.yml`
- **PostgreSQL**: `postgres/docker-compose.yml`
- **Redis**: `redis/docker-compose.yml`

## Usage

1. Navigate to the desired service folder, e.g.:
   ```powershell
   cd mysql
   ```
2. Start the service:
   ```powershell
   docker compose up -d
   ```
3. Stop the service:
   ```powershell
   docker compose down
   ```

## Customization
- Edit the `docker-compose.yml` files to change ports, credentials, or volumes as needed.
- Add more services or stacks as your needs grow.

---

Feel free to contribute or adjust these setups for your workflow!
