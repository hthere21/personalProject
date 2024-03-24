FROM  node:20-alpine

RUN addgroup app && adduser -S -G app app

USER app

WORKDIR /app

COPY package*.json ./

USER root

# Install Vite globally
RUN npm install -g vite

RUN npm install 

RUN chown -R app:app .

USER app

COPY . .

EXPOSE 5173

CMD npm run dev