FROM --platform=linux/amd64 mcr.microsoft.com/devcontainers/python:3.11

RUN sudo apt-get update && sudo apt-get install -y \
    git ffmpeg \
    libgl1 libglib2.0-0 \
    && sudo rm -rf /var/lib/apt/lists/*