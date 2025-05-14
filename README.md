# Voting System

This project demonstrates a microservices-based voting application using Docker, Redis, PostgreSQL, GitHub Actions for CI/CD, and optionally Kubernetes for zero-downtime deployments. It is designed to showcase container orchestration, continuous deployment, and scalability principles.

---

## Project Overview

This app allows users to vote between two options (e.g.,Cricket vs Football). The architecture includes multiple independent services connected through message queues and databases.

---

## Architecture

### Vote Service (Frontend)
- Built using Python Flask
- Provides a web interface for voting
- Sends vote data to Redis

### Worker Service
- Built using .NET Core
- Reads vote messages from Redis
- Stores processed votes into PostgreSQL

### Result Service (Backend Dashboard)
- Built using Node.js
- Displays live vote counts from PostgreSQL

### Redis
- In-memory message queue used for decoupling frontend and processing

### PostgreSQL
- Relational database used for storing final results

---

## Features

- Microservices-based design with Docker
- Fast message queuing using Redis
- Persistent vote storage using PostgreSQL
- Zero-downtime deployment ready
- GitHub Actions integrated for CI/CD pipelines
- Health checks and dependency handling
- Easy to extend and scale

- 
---

## Prerequisites

- Docker and Docker Compose installed
- Git installed
- (Optional) GitHub account for CI/CD
- (Optional) GHCR or DockerHub credentials for pushing images

---

## How to Run the Project Locally

### 1. Clone the repository

```bash
git clone https://github.com/devShashankhegde/final-devops.git
cd final-devops
docker-compose up --build

