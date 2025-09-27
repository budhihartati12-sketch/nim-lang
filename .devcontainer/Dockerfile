FROM mcr.microsoft.com/devcontainers/base:ubuntu-22.04

# Install dependencies
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get install -y curl git build-essential \
    && rm -rf /var/lib/apt/lists/*

# Install Nim (choosenim)
RUN curl https://nim-lang.org/choosenim/init.sh -sSf | bash -s -- -y \
    && echo 'export PATH=$HOME/.nimble/bin:$PATH' >> /home/vscode/.bashrc

ENV PATH="/home/vscode/.nimble/bin:${PATH}"
