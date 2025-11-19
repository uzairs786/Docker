# 📄 Understanding the Dockerfile

A **Dockerfile** is a text file containing step-by-step instructions for building a Docker image.
Each instruction creates a **new layer**, making builds repeatable, efficient, and easy to track—just like following a recipe.

---

## 🧱 Why Dockerfiles Matter

* They define **how an image is built**
* Ensure **consistent, repeatable environments**
* Allow you to recreate the exact same setup anytime
* Form the foundation of Docker-based workflows

---

## 🧩 Core Dockerfile Instructions

Below are the **five most common instructions** you’ll use:

### 1. `FROM`

Specifies the **base image**.

* Example: `FROM node:14`
* Foundation of your application (Python, Node, Ubuntu, etc.)

---

### 2. `RUN`

Executes commands while building the image.

* Install packages
* Update dependencies
* Example: `RUN npm install`

---

### 3. `COPY`

Copies files from your **host machine** into the container.

* Used to bring your app’s code/config into the image
* Example: `COPY . .`

---

### 4. `WORKDIR`

Sets the **working directory** inside the container.

* All following commands run in this directory
* Example: `WORKDIR /app`

---

### 5. `CMD`

Specifies the **command to run when the container starts**.

* Example for Python: `CMD ["python3", "app.py"]`
* Example for Node: `CMD ["node", "index.js"]`

---

## 📦 Example Dockerfile (Node.js)

```Dockerfile
FROM node:14

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 3000

CMD ["node", "index.js"]
```

### Explanation:

* `FROM` → Use Node 14 as the base image
* `WORKDIR` → Set `/app` as working directory inside the container
* `COPY package*.json` → Copy dependency files
* `RUN npm install` → Install Node dependencies
* `COPY . .` → Copy the rest of the application
* `EXPOSE 3000` → Container listens on port 3000
* `CMD` → Start the Node app

---

## ✅ Summary

* A Dockerfile defines the **recipe** for building an image
* Each instruction forms a **layer**
* Key commands: `FROM`, `RUN`, `COPY`, `WORKDIR`, `CMD`
* Ensures consistent and repeatable builds across all environments

---

