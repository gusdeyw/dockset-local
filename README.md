# Dockset Local

This repository contains ready-to-use Docker Compose setups for common development services. Use these to quickly spin up databases and tools for your projects.

## Available Stacks

- **MySQL**: `mysql/docker-compose.yml`
- **MariaDB**: `mariadb/docker-compose.yml`
- **PostgreSQL**: `postgres/docker-compose.yml`
- **Redis**: `redis/docker-compose.yml`
- **Nginx (Web Server)**: `nginx/docker-compose.yml`

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
- The `version` field in `docker-compose.yml` is optional and can be omitted for most setups.
- Add more services or stacks as your needs grow.

---

Feel free to contribute or adjust these setups for your workflow!
