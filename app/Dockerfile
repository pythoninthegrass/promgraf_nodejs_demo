# syntax=docker/dockerfile:1.7.0

FROM node:22-bookworm-slim

WORKDIR /app

COPY . .

RUN npm install --unsafe-perm

ENTRYPOINT ["node"]
