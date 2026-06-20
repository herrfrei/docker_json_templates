# Paperless-ngx

Paperless-ngx is a document management system that transforms your loose documents into a searchable, indexed, and organized collection.

## What's Included

This compose template includes:

- **Paperless-ngx** - Main application for document management
- **PostgreSQL** - Database for storing document metadata
- **Redis** - Broker for background tasks
- **Gotenberg** - PDF conversion service
- **Tika** - Document parsing service
- **Database backup** - Automated PostgreSQL backups

## Features

- **OCR** - Automatic text recognition from scanned documents
- **Metadata extraction** - Automatically extracts tags, dates, and more
- **Web interface** - Access your documents from anywhere
- **Document consumption** - Automatically process documents from a watched folder
- **Automated backups** - Daily backups of your database

## Installation

1. Copy the compose folder to your Docker host
2. Edit `.env` to customize paths and settings
3. Run `docker compose up -d`
4. Access the web interface at `http://localhost:8050`

## Configuration

See the `.env` file for all configurable options:

- Storage paths for data, media, export, and consume directories
- Database credentials
- User mapping (UID/GID)
- Timezone and OCR language

## Documentation

- [Paperless-ngx Documentation](https://docs.paperless-ngx.com/)
- [GitHub Repository](https://github.com/paperless-ngx/paperless-ngx)
