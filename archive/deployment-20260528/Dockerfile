FROM node:20-slim

# Install system dependencies
RUN apt-get update && apt-get install -y \
    git \
    curl \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /app

# Clone the repo
RUN git clone https://github.com/moltlaunch/cashclaw.git .

# Install dependencies
RUN npm install

# Install moltlaunch CLI (required by cashclaw)
RUN npm install -g @moltlaunch/cli

# Build the project
RUN npm run build:all

# Expose dashboard port
EXPOSE 3777

# Start the agent
CMD ["node", "dist/index.js"]
