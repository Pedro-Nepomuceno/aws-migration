# aws-migration

# MERN Application Deployment on AWS EC2

This repository documents the deployment and migration process of a MERN stack backend application running on AWS EC2.

The goal of this project is to:

* Learn production-style cloud deployment
* Practice cost-aware infrastructure decisions
* Document a real migration from **t2.micro → t3.micro**
* Prepare the application for **Docker containerization**
* Build a strong portfolio project demonstrating DevOps and cloud engineering practices

---

# Current Architecture

Frontend:

* Hosted on S3/Cloudfront

Backend:

* **Node.js / Express API**
* **PM2** process manager
* **Nginx** reverse proxy
* **Ubuntu EC2 instance**

Database:

* **MongoDB Atlas**

Traffic flow:

Internet
↓
Nginx (port 80 / 443)
↓
Node API (localhost:4000)
↓
MongoDB Atlas

---

# Why This Migration

The application was originally deployed on a **t2.micro instance**.

The goals of the migration are:

* Improve cost efficiency
* Rebuild the infrastructure cleanly
* Document deployment best practices
* Prepare the environment for Docker

---

# Migration Roadmap

Phase 1 — Document current deployment
Phase 2 — Launch new EC2 instance (t3.micro)
Phase 3 — Recreate runtime environment
Phase 4 — Deploy backend application
Phase 5 — Configure Nginx reverse proxy
Phase 6 — Enable HTTPS with Let's Encrypt
Phase 7 — Cut traffic to the new server
Phase 8 — Containerize application with Docker

---

# Cost Safeguards

To avoid unexpected charges the following protections are used:

* T3 instance in **Standard CPU credit mode**
* AWS **Budget alerts**
* Minimal infrastructure footprint
* Monitoring CPU and resource usage

---

# Technologies Used

* AWS EC2
* Ubuntu
* Node.js
* Express
* MongoDB Atlas
* Nginx
* PM2
* Git
* Docker (planned)

---

# Learning Goals

This project demonstrates:

* Linux server management
* Cloud cost optimization
* Reverse proxy configuration
* Secure HTTPS deployment
* Production-style backend deployment
* Containerization of an existing Node service

---

# Author

Pedro Lima

Cloud & Systems Enthusiast
