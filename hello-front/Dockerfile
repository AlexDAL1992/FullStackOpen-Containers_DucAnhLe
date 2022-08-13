FROM node:latest AS build-stage

WORKDIR /usr/src/app

COPY . .

RUN npm ci

RUN npm run build

FROM nginx:latest

COPY --from=build-stage /usr/src/app/build /usr/share/nginx/html
