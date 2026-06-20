# Paperless-ngx with SQLite

Paperless-ngx with SQLite is a document management system that transforms your loose documents into a searchable, indexed, and organized collection.

## What's Included

This compose template includes:

- **Paperless-ngx** - Main application for document management
- **Redis** - Broker for background tasks (required)
- **Gotenberg** - PDF conversion service
- **Tika** - Document parsing service

## Features

- **OCR** - Automatic text recognition from scanned documents
- **Metadata extraction** - Automatically extracts tags, dates, and more
- **Web interface** - Access your documents from anywhere
- **Document consumption** - Automatically process documents from a watched folder

## Installation

1. Copy the compose folder to your Docker host
2. Edit `.env` to customize paths and settings
3. Run `docker compose up -d`
4. Access the web interface at `http://localhost:8050`

## Configuration

See the `.env` file for all configurable options:

- Storage paths for data, media, export, consume, and redis directories
- User mapping (UID/GID)
- Timezone and OCR language

## When to use SQLite vs PostgreSQL

**Use SQLite if:**
- You have a small to medium document collection (< 10,000 documents)
- You're running a single-user instance
- You want the simplest possible setup
- Resource usage is a concern

**Use PostgreSQL instead if:**
- You have a large document collection
- Multiple users need to access Paperless
- You need reliable backups
- You want better performance with concurrent access

## Note on Redis

Even with SQLite, Redis is **required** as a message broker for background tasks like:
- Document processing
- OCR processing
- Email notifications
- Scheduled tasks

Redis is not used as a database here - it only handles background task queuing.

## Documentation

- [Paperless-ngx Documentation](https://docs.paperless-ngx.com/)
- [GitHub Repository](https://github.com/paperless-ngx/paperless-ngx)
