
# Docker NGINX Web Server

This repository provides a ready-to-use Docker setup for deploying an NGINX web server with persistent configuration, HTML content, and logging.

---

## Project Structure

```
docker-nginx/
├── docker-compose.yml
└── nginx/
    ├── Dockerfile
    ├── conf.d/
    │   └── default.conf
    ├── html/
    │   └── index.html
    └── logs/
```

---

## Prerequisites

- Docker
- Docker Compose

Ensure Docker is running on your machine before proceeding.

---

## Quick Start

### Step 1: Clone the Repository

```bash
git clone <your-repo-url>
cd docker-nginx
```

### Step 2: Run the Container

```bash
docker-compose up -d --build
```

The NGINX server will start and run in the background.

---

## Accessing the Web Server

Open a browser and navigate to:

```http
http://localhost:8080
```

You should see the default webpage confirming NGINX is running.

---

## Configuration and Persistence

| Directory | Description                                | Path in Container                |
|-----------|--------------------------------------------|----------------------------------|
| conf.d    | Persistent NGINX configuration files       | `/etc/nginx/conf.d`              |
| html      | Persistent HTML content served by NGINX    | `/usr/share/nginx/html`          |
| logs      | Persistent logs (access.log, error.log)    | `/var/log/nginx`                 |

Simply modify files in these folders to update configuration or content without needing to rebuild the container.

---

## Stopping the Container

To stop the NGINX server, run:

```bash
docker-compose down
```

---

## Troubleshooting

To check container status:

```bash
docker-compose ps
```

To view logs:

```bash
docker-compose logs nginx
```

---

## Licence

MIT License

Copyright (c) 2024

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
