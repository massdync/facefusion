FROM --platform=linux/amd64 mcr.microsoft.com/devcontainers/python:3.11

RUN sudo apt-get update && sudo apt-get install -y \
    git ffmpeg \
    libgl1 libglib2.0-0 \
    && sudo rm -rf /var/lib/apt/lists/*

# for Gradio
RUN sudo apt-get update && sudo apt-get install -y --no-install-recommends \
    curl ca-certificates \
&& sudo rm -rf /var/lib/apt/lists/*

RUN sudo mkdir -p /home/vscode/.cache/huggingface/gradio/frpc \
    && sudo curl -L --fail --retry 5 \
      -o /home/vscode/.cache/huggingface/gradio/frpc/frpc_linux_amd64 \
      https://cdn-media.huggingface.co/frpc-gradio-0.3/frpc_linux_amd64 \
    && sudo chmod +x /home/vscode/.cache/huggingface/gradio/frpc/frpc_linux_amd64 \
    && sudo chown -R vscode:vscode /home/vscode/.cache/huggingface