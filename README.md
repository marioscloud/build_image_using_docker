Build an Image Using a Dockerfile and Run the Image as a Container

***Overview***

This repository contains a hands-on lab that demonstrates how to build a Docker image using a Dockerfile and run the image as a container. The project involves a Node.js application that prints a hello message along with the hostname.

This hands-on lab is part of the Introduction to Containers with Docker, Kubernetes & OpenShift within the ***IBM DevOps and Software Engineering Professional Certificate***.

***Getting Started***

To get started with this project, follow the steps below.

Prerequisites

    -Docker installed on your machine.

    -Basic knowledge of Docker commands and Dockerfile instructions.

Building the Docker Image

    Navigate to the project directory where the Dockerfile is located:
    ```bash
    cd directory
    ```
    Build the Docker image using the following command:
    ```bash
    docker build . -t myimage:v1
    ```
    List images to see your image tagged myimage:v1 in the table.
    ```bash
    docker images
    ```

***Run the image as a container***

1. Now that your image is built, run it as a container with the following command:
    ```bash
    docker run -dp 8080:8080 myimage:v1
    ```
The output is a unique code allocated by docker for the application you are running. 

2. Run the curl command to ping the application as given below.
    ```bash
    curl localhost:8080
    ```
If you see the output ‘Your app is up and running!’, it indicates the app is running.

3. Now to stop the container we use docker stop followed by the container id. The following command uses docker ps -q to pass in the list of all running containers:

   ```bash
    docker stop $(docker ps -q)
    ```
4. Check if the container has stopped by running the following command.
      ```bash
    docker ps
    ```
