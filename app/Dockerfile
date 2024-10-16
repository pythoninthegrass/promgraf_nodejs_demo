# syntax=docker/dockerfile:1.7.0

FROM ubuntu:18.04

WORKDIR /app

ARG DEBIAN_FRONTEND=noninteractive

SHELL ["/bin/bash", "-o", "pipefail", "-c"]

RUN <<EOF
#!/bin/bash
apt-get update
apt-get install -y curl build-essential python git
curl -sL https://deb.nodesource.com/setup_12.x | bash -
apt-get install -y nodejs \
    rm -rf /var/lib/apt/lists/*
EOF

COPY . .

RUN npm install --unsafe-perm

ENTRYPOINT ["node"]
