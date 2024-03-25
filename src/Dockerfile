FROM ubuntu

ARG NODE_MAJOR=21

RUN apt update && apt install -y curl && \
    curl -fsSL https://deb.nodesource.com/setup_$NODE_MAJOR.x | bash - && \
    apt install -y nodejs

WORKDIR /app
COPY . .
RUN npm install
ENTRYPOINT [ "node", "server.js" ]
EXPOSE 8080