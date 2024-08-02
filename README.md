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
  - ![Screenshot from 2024-08-02 22-26-05](https://github.com/user-attachments/assets/649bb213-b397-4b67-a58f-2884b43041e7)

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
  - ![Screenshot from 2024-08-02 21-53-40](https://github.com/user-attachments/assets/27465eca-c7b6-4937-b0ec-9c245aed9dac)
  - lets edit file created and explain.
  - .....
## app.py
  - ![Screenshot from 2024-08-02 21-15-42](https://github.com/user-attachments/assets/3ad8092d-5914-4f29-836f-534673d96e79)
  - .....
## requirments.txt
  - ![Screenshot from 2024-08-02 21-23-40](https://github.com/user-attachments/assets/35c4a51a-ba7b-4313-8179-067c45f0bfb7)
  - "Flask" as said earlier is a web framework for phython
  - Werkzeug provides a foundation for Flask's request and response handling, routing, and other core functionality. Werkzeug is a dependency of Flask.
  - .....
## Dockerfile
  - ![Screenshot from 2024-08-02 21-39-59](https://github.com/user-attachments/assets/82020767-290d-438f-901d-d0017a80d9a5)
  - NOTE: "Dockerfile" does not have any extension.
  - see https://docs.docker.com/compose/gettingstarted/ for more understanding

# Build the Docker image and run it locally to ensure it works correctly.
  - Run "Docker build -t kodecamp-web . (to build the image created)
  - ![Screenshot from 2024-08-02 22-14-54](https://github.com/user-attachments/assets/9448bb6e-ac3c-4f3e-b6a6-71b4d1ffe6f4)
  - Our image is successfully build, lets verify by running "docker images".
  - ![Screenshot from 2024-08-02 22-37-02](https://github.com/user-attachments/assets/760d0c4c-0b6c-42ba-828c-af8bef35ee34)
## testing the build image
  - Run "docker run --name kodecamp-web -p 8000:5000 kodecamp-web (for spining up our build image and port forwarding)
  - ![Screenshot from 2024-08-02 22-46-31](https://github.com/user-attachments/assets/327c0696-831c-4875-9178-83c54d25e708)
  - visit http://yourhostip:8000 on your browser to test ur container.
  - ![Screenshot from 2024-08-02 20-46-02](https://github.com/user-attachments/assets/f9b2ab1d-8a1c-4a53-847e-6f48133bf5ae)
  - while on your browser you can also check your backend host, you should be seeing the request sent to the front end and the ip the request is coming from.
  - ![Screenshot from 2024-08-02 23-01-06](https://github.com/user-attachments/assets/c0e9f541-d74a-48d8-8e8b-748386b8151a)
  - Note: the container can also be runing in backgroud by add "-d" to the comand.
  - "docker run --name kodecamp-web -d -p 8000:5000 kodecamp-web (for runing container at first)
  - "docker run -d -p 8000:5000 kodecamp-web (for starting already provisioned container)
  - ![Screenshot from 2024-08-02 23-05-37](https://github.com/user-attachments/assets/901936e1-ecb8-49bd-bd99-f0f48a446d44)
  - to stop your container, run "docker stop (your container id)
    
# Tag it and Push the Docker image to a container registry
  - i need to open an account on https://hub.docker.com etails
  - ![Screenshot from 2024-08-02 23-09-25](https://github.com/user-attachments/assets/7b2a065b-cc6f-498b-a641-d56482a37cc0)
  - tag and push to docker hub
  - ![Screenshot from 2024-08-02 23-39-17](https://github.com/user-attachments/assets/3fa0347b-3a8b-4d46-b1fe-68c5b7c2229b)
  - log into your git hub account to verify if the repository was successfully push.
  - ![Screenshot from 2024-08-02 23-43-23](https://github.com/user-attachments/assets/b5369c44-b1b8-4082-9528-d35c9b5cd1b9)




 




  









 

