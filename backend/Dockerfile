FROM node:20-bookworm
RUN apt-get update && apt-get install -y --no-install-recommends \
    g++ gcc python3 python-is-python3 \
    && rm -rf /var/lib/apt/lists/*
WORKDIR /app
COPY package*.json ./
RUN npm ci --omit=dev
COPY . .
CMD ["npm", "start"]