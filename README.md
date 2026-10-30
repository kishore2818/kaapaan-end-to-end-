# Kaapaan End-to-End Project

## Overview
This repository contains the full source code for the Kaapaan application, including the backend API, frontend React UI, and supporting infrastructure (Docker, Nginx, CI). The folder structure is organized as follows:

```
useless/
├─ backend/          # Express + Socket.io server
│   ├─ server.js
│   ├─ package.json
│   └─ ...
├─ frontend/         # Vite + React application
│   ├─ src/          # React components, pages and lib
│   ├─ index.html
│   └─ package.json
├─ nginx/            # Nginx configuration for production
│   └─ default.conf
├─ docker-compose.yml
├─ Jenkinsfile       # CI/CD pipeline definition
└─ README.md         # (this file)
```

## Prerequisites
- **Node.js** (>= 20) and **npm**
- **Docker** and **docker‑compose** (optional, for containerised run)
- **Git**

## Running Locally
### Backend
```bash
cd backend
npm install          # install dependencies
npm start            # runs server.js (listens on PORT defined in .env)
```
### Frontend
```bash
cd frontend
npm install          # install dependencies
npm run dev          # start Vite dev server (http://localhost:5173)
# Or build for production
npm run build        # outputs to ../backend/dist
```
### Docker (All services)
```bash
docker-compose up --build
```
This will start Nginx, the backend, and the frontend containers as defined in `docker-compose.yml`.

## How to Clone and Contribute
```bash
git clone https://github.com/kishore2818/kaapaan-end-to-end-.git
cd kaapaan-end-to-end-
# Make changes, then:
git add .
git commit -m "Your descriptive message"
git push origin main
```

Feel free to open issues or submit pull requests for improvements.

