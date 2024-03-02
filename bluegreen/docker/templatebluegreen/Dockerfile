# FROM nginx:latest - vulnerable
FROM nginx:mainline-alpine

COPY index.html /usr/share/nginx/html

CMD ["nginx", "-g", "daemon off;"]