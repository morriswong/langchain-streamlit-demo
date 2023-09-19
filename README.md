---
title: langchain-streamlit-demo
emoji: 🦜
colorFrom: green
colorTo: red
sdk: docker
app_port: 7860
pinned: true
tags: [langchain, streamlit, docker]
---

# langchain-streamlit-demo

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![python](https://img.shields.io/badge/Python-3.11-3776AB.svg?style=flat&logo=python&logoColor=white)](https://www.python.org)
[![security: bandit](https://img.shields.io/badge/security-bandit-yellow.svg)](https://github.com/PyCQA/bandit)
[![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/charliermarsh/ruff/main/assets/badge/v1.json)](https://github.com/charliermarsh/ruff)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)
[![Checked with mypy](http://www.mypy-lang.org/static/mypy_badge.svg)](http://mypy-lang.org/)

[![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?&logo=docker&logoColor=white)](https://hub.docker.com/r/joshuasundance/langchain-streamlit-demo)
[![Docker Image Size (tag)](https://img.shields.io/docker/image-size/joshuasundance/langchain-streamlit-demo/latest)](https://hub.docker.com/r/joshuasundance/langchain-streamlit-demo)
[![Open HuggingFace Space](https://huggingface.co/datasets/huggingface/badges/raw/main/open-in-hf-spaces-sm.svg)](https://huggingface.co/spaces/joshuasundance/langchain-streamlit-demo)


This project shows how to build a simple chatbot UI with [Streamlit](https://streamlit.io) and [LangChain](https://langchain.com).

This `README` was written by [Claude 2](https://www.anthropic.com/index/claude-2), an LLM from [Anthropic](https://www.anthropic.com/).

# Features
- Chat interface for talking to AI assistant
- Supports models from
  - [OpenAI](https://openai.com/)
    - `gpt-3.5-turbo`
    - `gpt-4`
  - [Anthropic](https://www.anthropic.com/)
    - `claude-instant-v1`
    - `claude-2`
  - [Anyscale Endpoints](https://endpoints.anyscale.com/)
    - `meta-llama/Llama-2-7b-chat-hf`
    - `meta-llama/Llama-2-13b-chat-hf`
    - `meta-llama/Llama-2-70b-chat-hf`
- Streaming output of assistant responses
- Leverages LangChain for dialogue management
- Integrates with [LangSmith](https://smith.langchain.com) for tracing conversations
- Allows giving feedback on assistant's responses

# Usage
## Run on HuggingFace Spaces
[![Open HuggingFace Space](https://huggingface.co/datasets/huggingface/badges/raw/main/open-in-hf-spaces-sm.svg)](https://huggingface.co/spaces/joshuasundance/langchain-streamlit-demo)

## With Docker (pull from Docker Hub)
1. Run in terminal: `docker run -p 7860:7860 joshuasundance/langchain-streamlit-demo:latest`
2. Open http://localhost:7860 in your browser.

## Docker Compose
1. Clone the repo. Navigate to cloned repo directory.
2. Run in terminal: `docker compose up`
3. Then open http://localhost:7860 in your browser.

# Configuration
- Select a model from the dropdown
- Enter an API key for the relevant provider
- Optionally enter a LangSmith API key to enable conversation tracing
- Customize the assistant prompt and temperature

# Code Overview
- `app.py` - Main Streamlit app definition
- `llm_stuff.py` - LangChain helper functions

# Deployment
The app is packaged as a Docker image for easy deployment. It is published to Docker Hub and Hugging Face Spaces:

- [DockerHub](https://hub.docker.com/r/joshuasundance/langchain-streamlit-demo)
- [HuggingFace Spaces](https://huggingface.co/spaces/joshuasundance/langchain-streamlit-demo)

CI workflows in `.github/workflows` handle building and publishing the image.

# Links
- [Streamlit](https://streamlit.io)
- [LangChain](https://langchain.com)
- [LangSmith](https://smith.langchain.com)
- [OpenAI](https://openai.com/)
- [Anthropic](https://www.anthropic.com/)
- [Anyscale Endpoints](https://endpoints.anyscale.com/)

# TODO
1. More customization / parameterization in sidebar
