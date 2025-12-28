FROM node:18-slim

WORKDIR /usr/local/app

COPY package*.json ./

RUN npm ci && \
 npm cache clean --force 

COPY . .

ENV PORT=80
ENV DATABASE_URL=postgres://postgres:Krish@0303@10.174.240.3/postgres

RUN useradd -m appuser

USER appuser

EXPOSE 80

ENTRYPOINT ["node"]
CMD ["server.js"]
