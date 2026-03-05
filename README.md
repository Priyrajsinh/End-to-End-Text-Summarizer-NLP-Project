# 📝 End-to-End Text Summarizer — NLP Project

[![Python](https://img.shields.io/badge/Python-3.8-blue?logo=python&logoColor=white)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Framework](https://img.shields.io/badge/Framework-FastAPI-009688?logo=fastapi)](https://fastapi.tiangolo.com/)
[![Hugging Face](https://img.shields.io/badge/Model-HuggingFace_Transformers-yellow?logo=huggingface)](https://huggingface.co/)
[![Docker](https://img.shields.io/badge/Docker-Enabled-2496ED?logo=docker&logoColor=white)](https://www.docker.com/)

A production-ready, end-to-end **text summarization** application built with NLP and Transformer-based models. This project covers the full ML pipeline — from data ingestion and model training to a deployed web interface — making it a solid reference for building real-world NLP systems.

---

## 📌 Table of Contents

- [Overview](#overview)
- [Project Structure](#project-structure)
- [ML Pipeline Workflow](#ml-pipeline-workflow)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the Application](#running-the-application)
- [Docker Deployment](#docker-deployment)
- [CI/CD](#cicd)
- [Tech Stack](#tech-stack)
- [Author](#author)
- [License](#license)

---

## Overview

This project implements an **abstractive text summarization** system using pre-trained Transformer models from Hugging Face. It is structured as a modular, production-grade ML pipeline with clearly separated stages for data ingestion, validation, transformation, model training, and evaluation — all exposed through a FastAPI web application.

The goal is to provide a clean, reusable template for end-to-end NLP projects that can be easily extended, retrained, or deployed to a cloud environment.

---

## Project Structure

```
End-to-End-Text-Summarizer-NLP-Project/
│
├── .github/workflow/          # GitHub Actions CI/CD workflows
├── config/                    # YAML configuration files
├── research/                  # Jupyter notebooks for experimentation
├── src/textSummarizer/        # Core source package
│   ├── components/            # Pipeline stage components
│   ├── config/                # Configuration manager
│   ├── entity/                # Data entity definitions
│   └── pipeline/              # Stage pipeline scripts
│
├── summarizer_env/            # Conda environment files
├── app.py                     # FastAPI application entry point
├── main.py                    # Pipeline orchestrator
├── params.yaml                # Model hyperparameters
├── config/config.yaml         # Project-level configuration
├── requirements.txt           # Python dependencies
├── setup.py                   # Package setup
├── template.py                # Project scaffolding script
└── Dockerfile                 # Docker container configuration
```

---

## ML Pipeline Workflow

The project follows a modular pipeline design. Each stage is independently configurable and can be updated by modifying the corresponding files listed below.

| Step | File to Update | Description |
|------|---------------|-------------|
| 1 | `config/config.yaml` | Data paths, model artifacts, and output directories |
| 2 | `params.yaml` | Model training hyperparameters (epochs, batch size, etc.) |
| 3 | `src/textSummarizer/entity/` | Data class definitions for pipeline components |
| 4 | `src/textSummarizer/config/` | Configuration manager for reading YAML configs |
| 5 | `src/textSummarizer/components/` | Core logic for each pipeline stage |
| 6 | `src/textSummarizer/pipeline/` | Stage-level pipeline scripts |
| 7 | `main.py` | Full pipeline orchestration |
| 8 | `app.py` | FastAPI routes and web interface |

---

## Getting Started

### Prerequisites

Ensure you have the following installed on your machine:

- [Anaconda or Miniconda](https://docs.conda.io/en/latest/miniconda.html)
- Python 3.8
- Git

### Installation

**Step 1 — Clone the repository:**

```bash
git clone https://github.com/Priyrajsinh/End-to-End-Text-Summarizer-NLP-Project.git
cd End-to-End-Text-Summarizer-NLP-Project
```

**Step 2 — Create and activate a Conda environment:**

```bash
conda create -n summary python=3.8 -y
conda activate summary
```

**Step 3 — Install dependencies:**

```bash
pip install -r requirements.txt
```

### Running the Application

**Train the full pipeline:**

```bash
python main.py
```

**Launch the web application:**

```bash
python app.py
```

Once running, open your browser and navigate to:

```
http://localhost:8080
```

You will be presented with a web UI where you can input any text and receive an abstractive summary in return.

---

## Docker Deployment

A `Dockerfile` is included to containerize the application for consistent, environment-agnostic deployment.

**Build the Docker image:**

```bash
docker build -t text-summarizer .
```

**Run the container:**

```bash
docker run -p 8080:8080 text-summarizer
```

The application will be accessible at `http://localhost:8080`.

---

## CI/CD

This project includes a GitHub Actions workflow (`.github/workflow/`) for automated testing and deployment. The pipeline is designed to be integrated with AWS or any cloud provider supporting Docker-based deployments.

---

## Tech Stack

| Category | Technology |
|----------|-----------|
| Language | Python 3.8 |
| NLP Framework | Hugging Face Transformers |
| Web Framework | FastAPI |
| Frontend | HTML, CSS, JavaScript (Jinja2 templates) |
| Experiment Tracking | Jupyter Notebooks |
| Containerization | Docker |
| Configuration | YAML |
| CI/CD | GitHub Actions |

---

## Author

**Priyrajsinh Parmar**  
Machine Learning & NLP Enthusiast  
📧 [priyrajsinh03@gmail.com](mailto:priyrajsinh03@gmail.com)  
🔗 [GitHub Profile](https://github.com/Priyrajsinh)

---

## License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and distribute this project with proper attribution.

---

> ⭐ If you found this project helpful, consider giving it a star on GitHub!
