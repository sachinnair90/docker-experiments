FROM node:alpine AS initial

WORKDIR /app

COPY ./src/sample-app/package.json package.json
COPY ./src/sample-app/package-lock.json package-lock.json

RUN npm i

COPY ./src/sample-app .

RUN npm run build

FROM nginx:alpine AS final

COPY --from=initial /app/dist/sample-app /usr/share/nginx/html
