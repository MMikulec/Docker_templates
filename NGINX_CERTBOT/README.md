# NGINX and Certbot Docker Compose Template

This repository provides a Docker Compose template for setting up an NGINX web server along with Certbot for SSL certificate management. This setup is ideal for deploying web applications securely with ease.

## Features

- **NGINX**: Latest NGINX as a reverse proxy
- **Certbot**: Automatic SSL certificate issuance and renewal with Certbot
- **Docker Compose**: Easy setup and configuration through Docker Compose

## Pre-requisites

- Docker and Docker Compose installed on your system
- A domain name pointing to the machine where Docker is running

## Project Structure

```
NGINX_CERTBOT/
├── docker-compose.yml  # Docker Compose file
└── nginx/              # NGINX configuration files
└── default.conf    # Default NGINX configuration
```

## Quick Start

1. **Clone the Specific Folder**

```bash
# Make sure you are in the correct directory
```

2. **Edit the `default.conf`**

Update the `default.conf` in the `nginx/` directory to match your application's configuration.

3. **Start the Containers**

```bash
docker-compose up -d
```

4. **Initial SSL Certificate Setup**

Uncomment the Certbot service entrypoint in `docker-compose.yml` after obtaining your initial SSL certificate.

5. **Reload NGINX**

```bash
docker-compose exec nginx nginx -s reload
```
