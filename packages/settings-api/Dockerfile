# syntax=docker/dockerfile:1

# Run Node.js app
# ------------------------------------
FROM node:22-alpine
ENV NODE_ENV=dev
WORKDIR /app
COPY ./package*.json ./
COPY ./packages/settings-api ./packages/settings-api
RUN npm ci --workspace=settings-api --cache /tmp/empty-cache
EXPOSE 4001
CMD [ "npm", "start", "--workspace=settings-api" ]
