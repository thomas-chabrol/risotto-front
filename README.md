# Risotto Front : React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Exemple config to run project with Docker

### Dockerfile
```
FROM node:16-alpine3.16

WORKDIR /app
COPY package*.json ./

COPY . .
EXPOSE 8080

CMD ["npm", "serve"]
```

### docker-compose.yml
```
risotto_front:
    build: ./risotto-front/
    container_name: risotto_front
    ports:
        - '8125:8080'
    volumes:
        - ./risotto-front:/app
```