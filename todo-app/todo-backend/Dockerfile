FROM node:18
WORKDIR /usr/src/app
COPY --chown=node:node . .
RUN npm ci
ENV DEBUG=todo-backend:*
USER node
CMD npm start
