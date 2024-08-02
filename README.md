# containerization-project
# objectives
## Create a simple web application:
  - Use Python Programming Language to create your simple application
  - The application should display a simple message like "Hello, Welcome to KodeCamp DevOps Bookcamp!"
  - You can give your app more features if you choose to.
## Dockerize the application:
  - Write a Dockerfile to containerize the application.
  - Build the Docker image and run it locally to ensure it works correctly.
  - Tag it and Push the Docker image to a container registry (e.g., Docker Hub).
## Deploy the application to a Kubernetes cluster:
  - Create a Kubernetes manifest file for a Deployment to deploy the Docker image.
  - Deploy the app to your minikube cluster
  - Create a Kubernetes Service of type ClusterIP to expose the application.
## Test the deployment:
  - Port-forward your service to a localhost port and access it through your web browser.
  - Verify that the application displays the expected message.

# steps in Acheivng the above objectives
## Directory and file structure for the project.
  -  ![Screenshot from 2024-08-02 22-26-05](https://github.com/user-attachments/assets/4d8da70f-e005-41a6-b6e1-98671399f4d3)

## Requirements
  - docker
  - docker compose
  - linux host
  - see https://docs.docker.com/manuals/
    
to make the project more realistic lets use a web template.
log-on to https://templatemo.com to download any template of ur choice.
in my case i chose the bellow template.
unzip it, in my case i also made some changes.
  - ![Screenshot from 2024-08-01 21-07-00](https://github.com/user-attachments/assets/f04ba16a-f7cb-4f96-8ccf-ba54b4092d6f)
  - create a directory "kodecamp-web", cd into the directory and create file with respect to the above project structure
  - unzip the downloaded template and place it in the directory.
  - ![Screenshot from 2024-08-01 21-07-00](https://github.com/user-attachments/assets/ae776bd1-cc7c-4bb1-8e42-d29c2fa8dc86)
  - lets edit file created and explain.
  - .....
## app.py
  - ![Screenshot from 2024-08-02 21-15-42](https://github.com/user-attachments/assets/9e90db1b-e281-4e0b-830c-c992a8dc4fed)
  - .....
## requirments.txt
  - ![Screenshot from 2024-08-02 21-23-40](https://github.com/user-attachments/assets/01f722ef-7c0d-4f94-a220-e812b2af4c59)

  - "Flask" as said earlier is a web framework for phython
  - Werkzeug provides a foundation for Flask's request and response handling, routing, and other core functionality. Werkzeug is a dependency of Flask.
  - .....
## Dockerfile
  - ![Screenshot from 2024-08-02 21-39-59](https://github.com/user-attachments/assets/f7f0a52b-e0a6-4981-bae4-5c7432ceea84)

  - NOTE: "Dockerfile" does not have any extension.
  - see https://docs.docker.com/compose/gettingstarted/ for more understanding

# Build the Docker image and run it locally to ensure it works correctly.
  - Run "Docker build -t kodecamp-web . (to build the image created)
  - ![Screenshot from 2024-08-02 22-14-54](https://github.com/user-attachments/assets/68190030-1dfe-4c09-851d-ae003fb785e1)

  - Our image is successfully build, lets verify by running "docker images".
  - ![Screenshot from 2024-08-02 22-37-02](https://github.com/user-attachments/assets/028b903c-b4c5-49c5-acc7-a8811dd9cb20)

## testing the build image
  - Run "docker run --name kodecamp-web -p 8000:5000 kodecamp-web (for spining up our build image and port forwarding)
  - ![Screenshot from 2024-08-02 22-46-31](https://github.com/user-attachments/assets/93581f19-8244-4249-bd45-93bbdda598ec)

  - visit http://yourhostip:8000 on your browser to test ur container.
  - ![Screenshot from 2024-08-02 20-46-02](https://github.com/user-attachments/assets/6668d909-b3cb-4e09-90c3-f4eeffe2cc1a)

  - while on your browser you can also check your backend host, you should be seeing the request sent to the front end and the ip the request is coming from.
  - !![Screenshot from 2024-08-02 23-01-06](https://github.com/user-attachments/assets/81bca0ea-6a64-4744-a85e-56ca0f43dc19)

  - Note: the container can also be runing in backgroud by add "-d" to the comand.
  - "docker run --name kodecamp-web -d -p 8000:5000 kodecamp-web (for runing container at first)
  - "docker run -d -p 8000:5000 kodecamp-web (for starting already provisioned container)
  - run "docker ps -a" to check the processess runing in background.
  - ![Screenshot from 2024-08-02 23-05-37](https://github.com/user-attachments/assets/61937c6f-5d34-4586-80b1-e90cc6f9861e)
  - to stop your container, run "docker stop (your container id)
    
# Tag it and Push the Docker image to a container registry
  - i need to open an account on https://hub.docker.com and login your account details to link your host.
  - ![Screenshot from 2024-08-02 23-09-25](https://github.com/user-attachments/assets/5534239a-cfd5-4821-aae7-dd2adacab643)

  - tag and push to docker hub
  - ![Screenshot from 2024-08-02 23-39-17](https://github.com/user-attachments/assets/1ec16a68-06f3-47c1-9019-951b9f9ab395)

  - log into your git hub account to verify if the repository was successfully push.
  - ![Screenshot from 2024-08-02 23-43-23](https://github.com/user-attachments/assets/c93f3875-fc03-4165-a206-f9a7e41733b4)





 




  









 

