# Dockset Local

This repository contains ready-to-use Docker Compose setups for common development services. Use these to quickly spin up databases, web servers, storage solutions, and development tools for your projects.

## Available Services

### Databases
- **MySQL**: `mysql/docker-compose.yml` - Popular relational database
- **MariaDB**: `mariadb/docker-compose.yml` - MySQL-compatible database
- **PostgreSQL**: `postgres/docker-compose.yml` - Advanced relational database
- **MongoDB**: `mongodb/docker-compose.yml` - NoSQL document database
- **Redis**: `redis/docker-compose.yml` - In-memory data store and cache

### Web Servers & Applications
- **Nginx**: `nginx/docker-compose.yml` - High-performance web server
- **WordPress**: `wordpress/docker-compose.yml` - WordPress with MariaDB backend

### Storage & File Management
- **MinIO**: `minio/docker-compose.yml` - S3-compatible object storage server

### Database Management Tools
- **Adminer**: `adminer/docker-compose.yml` - Database management interface
- **Mongo Express**: `mongoexpress/docker-compose.yml` - MongoDB web admin interface

## Quick Start

1. Navigate to the desired service folder:
   ```powershell
   cd <service-name>
   ```
2. Start the service in detached mode:
   ```powershell
   docker compose up -d
   ```
3. Stop the service:
   ```powershell
   docker compose down
   ```
4. Stop and remove volumes (⚠️ this will delete data):
   ```powershell
   docker compose down -v
   ```

## Service Details & Access

### Databases
- **MySQL**: Port 3306, user: `root`, password: `rootpassword`
- **MariaDB**: Port 3307, user: `root`, password: `rootpassword`
- **PostgreSQL**: Port 5432, user: `postgres`, password: `postgres`
- **MongoDB**: Port 27017, no authentication by default
- **Redis**: Port 6379, no authentication by default

### Web Services
- **Nginx**: http://localhost:8080
- **WordPress**: http://localhost:8090 (with MariaDB backend)
- **MinIO Console**: http://localhost:9051 (user: `minioadmin`, password: `minioadmin123`)
- **MinIO API**: http://localhost:9050

### Management Tools
- **Adminer**: http://localhost:8081 (database management for all SQL databases)
- **Mongo Express**: http://localhost:8082 (MongoDB web interface)


## Data Persistence

All services use Docker volumes for data persistence. Your data will be retained between container restarts unless you explicitly remove the volumes with `docker compose down -v`.

## Security Notes

⚠️ **Important**: These configurations are designed for local development only. Default passwords and settings are used for convenience.

For production use:
- Change all default passwords
- Configure proper authentication
- Use environment variables for sensitive data
- Review and adjust network exposure

## File Structure

```
dockset-local/
├── adminer/           # Database management UI
├── mariadb/          # MariaDB database
├── minio/            # Object storage server
├── mongodb/          # MongoDB NoSQL database
├── mongoexpress/     # MongoDB web interface
├── mysql/            # MySQL database
├── nginx/            # Web server with sample site
├── postgres/         # PostgreSQL database
├── redis/            # Redis cache/data store
├── wordpress/        # WordPress CMS with MariaDB
└── README.md         # This file
```

## Customization

- Edit the `docker-compose.yml` files to change ports, credentials, or volumes as needed
- The `version` field in `docker-compose.yml` is optional for modern Docker Compose
- Add environment files (`.env`) for sensitive configuration
- Modify service configurations to match your development needs

## Contributing

Feel free to contribute additional services or improvements to existing configurations. Make sure to:
- Test your configurations locally
- Update this README with new services
- Follow the existing naming and structure conventions

---

**Happy containerizing! 🐳**
