FROM node:18-alpine AS build

WORKDIR /app

COPY package.json ./

COPY package-lock.json ./

RUN npm install

COPY . .
CMD [ "npm" ,"run", "dev" ,"--","--host" ,"0.0.0.0" ]

# FROM nginx:alpine
# COPY --from=build /app/build /usr/share/nginx/html
# EXPOSE 80
# CMD ["nginx", "-g", "daemon off;"]

