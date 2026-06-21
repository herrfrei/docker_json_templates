# docker_json_templates

This repository contains Docker Compose templates for various applications optimized for MOS (My Home Server).

## Available Templates

### Forgejo
- **Location:** `compose/forgejo/`
- **Description:** A lightweight, self-hosted Git service. A community-driven fork of Gitea, designed to be minimal and resource-efficient.
- **Features:** Ultra-lightweight, Web UI, Git SSH access, issue tracking, pull requests, minimal dependencies
- **Services:** Forgejo (single container with SQLite database)

### Immich
- **Location:** `compose/immich/`
- **Description:** Self-hosted photo and video management system with AI-powered organization
- **Features:** GPU acceleration support, machine learning for facial recognition, automatic backups

### Paperless-ngx (PostgreSQL)
- **Location:** `compose/paperless/`
- **Description:** Document management system for organizing, scanning, and archiving documents
- **Features:** OCR, metadata extraction, web-based access, document consumption, automatic backups
- **Services:** Paperless-ngx, PostgreSQL, Redis, Gotenberg (PDF conversion), Tika (document parsing), Backup service

### Paperless-ngx (SQLite)
- **Location:** `compose/paperless-sqlite/`
- **Description:** Simplified Paperless-ngx setup with SQLite database
- **Features:** Single container setup, no external database needed, ideal for smaller deployments
- **Services:** Paperless-ngx, Gotenberg (PDF conversion), Tika (document parsing)

## Usage

1. Copy the desired template folder to your Docker host
2. Review and adjust the `.env` file with your preferred settings
3. Run `docker compose up -d` to start the services
4. Access the web interface at the URL specified in the template's `template.json`

## Maintainer

- **Name:** herrfrei
