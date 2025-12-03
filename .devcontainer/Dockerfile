FROM mcr.microsoft.com/devcontainers/python:0-3.11

RUN apt-get update \
    && apt-get install -y --no-install-recommends build-essential git \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

COPY requirements.txt /tmp/requirements.txt
RUN if [ -f /tmp/requirements.txt ]; then pip install --no-cache-dir -r /tmp/requirements.txt || true; fi

ENV DEBIAN_FRONTEND=noninteractive

USER vscode
