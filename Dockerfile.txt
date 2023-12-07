# Use a lightweight base image with Nginx
FROM nginx:alpine

# Copy the local index.html file to the container's web root
COPY index.html /usr/share/nginx/html/

# Expose port 80 to make the web server accessible
EXPOSE 80

# Command to start the web server
CMD ["nginx", "-g", "daemon off;"]
