# GitOps-project – Smart Manufacturing Machines Efficiency Prediction

This project implements a **GitOps-driven workflow** for building, training, and deploying machine learning models that predict the efficiency of manufacturing machines using sensor data. It integrates automation, CI/CD, and containerization principles tailored for Industry 4.0 applications.

---

## Objectives

- Predict machine efficiency (e.g., OEE – Overall Equipment Effectiveness)
- Analyze real-time sensor data: temperature, vibration, energy use, uptime
- Automate training and deployment via Jenkins and GitOps principles
- Support containerized deployment to cloud or edge via Docker/Kubernetes

## Technology Stack

- **ML & Data**: `pandas`, `scikit-learn`, `xgboost`, `numpy`
- **API**: `Flask` or `FastAPI`
- **Visualization**: `matplotlib`, `plotly`
- **DevOps**: `Docker`, `Jenkins`, `Kubernetes`
- **GitOps tools** (optional): `ArgoCD`, `Flux`

--
graph TD
  GitHub -->|Code push| Jenkins
  Jenkins -->|Build/Test| Docker
  Docker -->|Push image| DockerHub
  DockerHub -->|Trigger| Kubernetes
  Kubernetes -->|Run|[ML API Service]