# 🛠️ Ansible Task Deployment

This repository contains an automated Ansible setup to configure and deploy a simple Flask-based web application inside a Docker container.

---

## 🚀 Tech Stack

<p float="left">
  <img src="https://img.shields.io/badge/Ansible-EE0000?style=for-the-badge&logo=ansible&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white"/>
  <img src="https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white"/>
</p>

---

## 📂 Project Tree

```
├── CONTRIBUTORS.md
├── README.md
├── playbook
│   ├── ansible.cfg
│   ├── hosts.ini
│   └── playbook.yml
└── setup
    ├── Dockerfile.ansible
    ├── Dockerfile.deb
    ├── docker-compose.yml
    ├── id_rsa
    ├── id_rsa.pub
    └── node.sh
```

---

## ⚙️ Requirements

- Docker
- Docker Compose
- Git

---

## 📦 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/ronthesoul/ansible_task.git
cd ansible_task/setup
```

### 2. Build and Start the Container

```bash
docker compose up --build -d
```

### 3. Enter the Docker Container

```bash
docker exec -it ansible_task_container bash
```

> Replace `ansible_task_container` with your container name if different.

### 4. Run the Ansible Playbook

```bash
cd ansible_task/playbook
ansible-playbook playbook.yml
```

---

## 🌐 Access the Web App

Visit: [http://localhost:8000](http://localhost:8000)

---

## 📘 Notes

- Ensure Docker is installed and running before starting.
- You can customize variables in `playbook.yml` to suit your environment.
- Make sure to allow ports 5000 if using a VM or remote server.

---

## 🧠 Useful Commands

```bash
# View running containers
docker ps

# Rebuild containers
docker compose up --build

# Stop all containers
docker compose down
```


---

## 👤 Author
Created by [ronthesoul](https://github.com/ronthesoul).
