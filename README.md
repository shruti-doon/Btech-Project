# Crop Darpan: DevOps Automation with Jenkins, Docker, and Kubernetes

A **B.Tech project** demonstrating a complete, automated DevOps lifecycle for the "Crop Darpan" agricultural platform.  
This project architects a **CI/CD pipeline** using **Jenkins**, containerizes the application with **Docker**, and manages deployment and scaling using **Kubernetes**.

---


##  Project Overview

**Crop Darpan** is a conceptual agricultural platform designed to **connect farmers with real-time crop data, weather information, and market prices**.  

This repository focuses on the **DevOps strategy** for the platform — moving from traditional, manual deployment to a modern, **automated, scalable, and resilient** system capable of continuous development.

---

##  Problem Statement

In a traditional software lifecycle, developers, testers, and operations teams often work in silos. This leads to several challenges:

-  **Slow Deployments** — Manual hand-offs and builds take time.  
-  **Inconsistent Environments** — The "it works on my machine" problem caused by environment differences.  
-  **Difficult Scaling** — Manually adjusting servers to meet demand is inefficient.  
-  **Poor Reliability** — A single server failure can bring down the entire application.

This project solves these problems by designing a **fully automated CI/CD pipeline**.

---

##  Solution Architecture

The implemented CI/CD workflow automates the entire development lifecycle:

1. **Commit:** Developer pushes code to GitHub.  
2. **Trigger:** A webhook notifies Jenkins of the new commit.  
3. **Build:** Jenkins checks out the code, builds the app, and runs tests.  
4. **Package:** Jenkins builds a Docker image containing the app and its dependencies.  
5. **Push:** Docker image is pushed to Docker Hub.  
6. **Deploy:** Jenkins instructs Kubernetes to pull the new image and perform a rolling update.  
7. **Orchestrate:** Kubernetes handles scaling, self-healing, and load balancing.


##  The CI/CD Pipeline Explained

The entire pipeline is defined as **code**, making it repeatable and version-controlled.

### 1️ Jenkinsfile (Declarative Pipeline)
The Jenkinsfile is the **brain** of the operation — it lives in the root of the repository and defines each pipeline stage.

