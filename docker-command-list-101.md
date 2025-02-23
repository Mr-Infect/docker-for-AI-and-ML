# 🐳 Docker Commands for AI/ML Engineers 🚀

This repository contains a collection of useful Docker commands specifically curated for AI/ML engineers. These commands help in setting up deep learning environments, optimizing GPU usage, and managing Docker containers efficiently.

## 📌 **Table of Contents**
1. [Container Management](#container-management)
2. [Image Handling](#image-handling)
3. [Networking & Volumes](#networking--volumes)
4. [GPU & AI/ML Specific](#gpu--aiml-specific)
5. [Performance Optimization](#performance-optimization)

---

## 🛠️ **1. Container Management**

| Command | Description |
|---------|-------------|
| `docker ps` | List all running containers |
| `docker ps -a` | List all containers (including stopped ones) |
| `docker stop <container_id>` | Stop a running container |
| `docker start <container_id>` | Start a stopped container |
| `docker restart <container_id>` | Restart a container |
| `docker rm <container_id>` | Remove a stopped container |
| `docker logs <container_id>` | View logs of a running container |
| `docker exec -it <container_id> bash` | Access an interactive shell inside a running container |

---

## 📦 **2. Image Handling**

| Command | Description |
|---------|-------------|
| `docker images` | List all downloaded images |
| `docker rmi <image_id>` | Remove an image |
| `docker pull tensorflow/tensorflow:latest-gpu` | Pull the latest TensorFlow image with GPU support |
| `docker build -t my-ml-image .` | Build a custom AI/ML image from a Dockerfile |
| `docker commit <container_id> my-ml-image:v1` | Save changes made to a container as a new image |

---

## 🌐 **3. Networking & Volumes**

| Command | Description |
|---------|-------------|
| `docker network ls` | List all Docker networks |
| `docker network create my-ml-network` | Create a custom Docker network |
| `docker run -v $(pwd):/app -w /app my-ml-image` | Mount the current directory inside the container |
| `docker volume create ml-data` | Create a persistent volume for datasets |
| `docker run -v ml-data:/data my-ml-image` | Attach a persistent volume to a container |

---

## 🎯 **4. GPU & AI/ML Specific**

| Command | Description |
|---------|-------------|
| `docker run --gpus all -it tensorflow/tensorflow:latest-gpu bash` | Run a TensorFlow GPU container interactively |
| `docker run --gpus all -it nvidia/cuda:12.1-devel bash` | Run a CUDA-enabled container for ML training |
| `docker run --gpus all -v $(pwd):/workspace my-ml-image` | Bind mount current directory with GPU support |
| `docker run --shm-size=8g --gpus all -it my-ml-image` | Allocate shared memory (important for PyTorch) |
| `docker exec -it <container_id> nvidia-smi` | Check GPU usage inside a running container |

---

## ⚡ **5. Performance Optimization**

| Command | Description |
|---------|-------------|
| `docker system prune -a` | Remove unused containers, networks, and images to free space |
| `docker stats` | Monitor container performance (CPU, memory, network) |
| `docker cp <container_id>:/app/model.pth ./` | Copy trained ML model from container to host |
| `docker run --ipc=host --ulimit memlock=-1:-1 my-ml-image` | Avoid memory locking issues in ML workloads |
| `docker-compose up` | Start services using a `docker-compose.yml` file |

---

## 📢 **Contribute**
If you have more useful Docker commands for AI/ML engineers, feel free to contribute by submitting a pull request! 🚀

---
