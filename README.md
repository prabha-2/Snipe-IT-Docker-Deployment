# Snipe-IT – Docker Deployment on AWS EC2

## Overview

Explored and deployed **Snipe-IT**, an open-source IT Asset Management (ITAM) application.

Snipe-IT helps organizations manage IT assets such as laptops, desktops, servers, accessories, software licenses, and asset assignments.

## Why Snipe-IT?

- Centralized IT asset tracking.
- Manage asset assignments and returns.
- Track asset details and availability.
- Maintain records of organizational IT equipment.

## Architecture

```text
             User / Browser
                   |
                HTTP :8000
                   |
             AWS EC2 (Ubuntu)
                   |
              Docker Compose
                   |
          Docker Internal Network
                   |
          +--------+---------+
          |                  |
          v                  |
      Snipe-IT  <----------> MariaDB
      Container    db:3306   Container
          |                  |
          v                  v
      Storage Volume     DB Volume
```

## Deployment

1. Launch an Ubuntu EC2 instance on AWS.
2. Install Docker Engine and Docker Compose.
3. Download the official Snipe-IT Docker Compose configuration.
4. Configure application and database environment variables.
5. Start the application using Docker Compose.
6. Complete the web-based installation wizard.
7. Access Snipe-IT through the EC2 public IP on port `8000`.

## Technologies Used

- AWS EC2
- Ubuntu
- Docker
- Docker Compose
- Snipe-IT
- MariaDB


## References

- [Official Snipe-IT Repository](https://github.com/grokability/snipe-it)
- [Snipe-IT Docker Documentation](https://snipe-it.readme.io/docs/docker)
