A Dockerfile contains several instructions to define how an image should be built. 


![image](https://github.com/user-attachments/assets/2dd1e23d-5f29-4530-afaa-a44f1e9dd18a)

Here’s a summary of the most common Dockerfile instructions:
1. FROM: Sets the base image for the new image.
2. RUN: Executes commands in a new layer on top of the current image.
4. LABEL: Adds metadata to the image.
5. EXPOSE: Indicates the ports the container will listen on at runtime.
6. ENV: Sets environment variables.
7. ADD: Copies files/directories into the image and automatically extracts compressed files.
8. COPY: Copies files/directories into the image without extracting.
10. VOLUME: Creates a mount point for external storage.
11. USER: Sets the username or UID to use when running the image.
12. WORKDIR: Sets the working directory for subsequent instructions.
13. ARG: Defines a variable that users can pass at build-time to the Dockerfile.
3. CMD: Provides default commands to run when a container is started.
9. ENTRYPOINT: Configures a container to run as an executable.



# example nginx file

# Use the official Nginx image from the Docker Hub
FROM nginx:latest

# Set the maintainer label
LABEL maintainer="yourname@example.com"

# Set environment variables
ENV NGINX_HOST=localhost
ENV NGINX_PORT=80

# Copy static HTML files to the Nginx HTML directory
COPY ./html /usr/share/nginx/html

# Add a configuration file (it can also extract compressed files if needed)
# ADD url 

# Expose port 80
EXPOSE 80

# Set the working directory
WORKDIR /usr/share/nginx/html

# Create a mount point for external storage
VOLUME ["/usr/share/nginx/html"]

# Set the user for the container
USER nginx

# Start Nginx when the container runs
ENTRYPOINT ["nginx", "-g", "daemon off;"]
#CMD ["nginx", "-g", "daemon off;"] --(it run single arguement)

# ARG for build-time variables
ARG VERSION=latest
