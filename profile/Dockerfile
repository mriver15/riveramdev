# Use a lightweight nginx image
FROM nginx:alpine

# Remove the default nginx website
RUN rm -rf /usr/share/nginx/html/*

# Copy the React production build to nginx
COPY build/ /usr/share/nginx/html/

# Copy custom nginx config (optional)
# COPY nginx.conf /etc/nginx/nginx.conf

# Expose port 80
EXPOSE 80

# Start nginx
CMD ["nginx", "-g", "daemon off;"]