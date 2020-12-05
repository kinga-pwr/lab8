# Stage 0: compile angular frontend
FROM node:latest as build
WORKDIR /app
COPY . . 
RUN npm install
RUN npm install -g @angular/cli@7.3.9
RUN ng build


# Stage 1: serve app with nginx server
FROM nginx:latest
COPY --from=build /app/dist  /usr/share/nginx/html
COPY nginx.conf /etc/nginx/conf.d/default.conf
EXPOSE 8080