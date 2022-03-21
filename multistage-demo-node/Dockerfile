# Buildtime
FROM node:16-alpine as builder
WORKDIR app
COPY package*.json .
COPY index.js .
RUN npm install && npm run build

# Runtime
FROM node:16-alpine
COPY --from=builder /app/index.build.min.js .

EXPOSE 8080
CMD [ "node", "index.build.min.js" ]