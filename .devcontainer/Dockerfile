FROM mcr.microsoft.com/devcontainers/base:ubuntu-22.04

# Install dependencies
RUN apt-get update && apt-get install -y \
    curl git build-essential \
    && rm -rf /var/lib/apt/lists/*

# Switch ke user vscode (default di devcontainers)
USER vscode
WORKDIR /workspaces

# Install Nim via choosenim untuk user vscode
RUN curl https://nim-lang.org/choosenim/init.sh -sSf | bash -s -- -y \
    && echo 'export PATH=$HOME/.nimble/bin:$PATH' >> ~/.bashrc

ENV PATH="/home/vscode/.nimble/bin:${PATH}"
