# Build step
FROM node:18 AS builder
WORKDIR /app
COPY . .
RUN npm install && npm run build

# Serve with NGINX
FROM nginx:stable-alpine
COPY --from=builder /app/build /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]