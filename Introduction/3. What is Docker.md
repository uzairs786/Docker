# 🐳 What Is Docker?

Docker is the most widely used platform for **building**, **shipping**, and **running** containerized applications.
It makes containers easy to create, manage, distribute, and run in any environment.

---

## 🔧 Docker Engine

The **Docker Engine** is the core service that powers Docker.

* Responsible for **creating**, **running**, and **managing** containers
* Uses **Dockerfiles** and **images** to build containers
* Comparable to a car engine: it drives everything behind the scenes

Without the Docker Engine, containers cannot run.

---

## 🏬 Docker Hub

**Docker Hub** is Docker’s cloud-based repository for container images.

* Similar to an **App Store** or **Google Play**, but for container images
* Includes:

  * Official images (e.g., Ubuntu, Python, Nginx)
  * Community images
  * Your own images (you can push/publish them)

You can **pull** images to your environment or **upload** your own.

---

## 🧩 Docker Compose

**Docker Compose** is a tool for managing **multi-container** applications.

* Lets you define multiple services in a single `docker-compose.yml` file
* Describes:

  * How services interact
  * What resources they need
  * How they should run together

Example: a web app + database + cache, all orchestrated together.

Think of Docker Compose as the **recipe** for running an entire application stack.

---


