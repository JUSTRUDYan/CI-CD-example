# CI/CD Example Project Documentation
## Project Overview
This project demonstrates a Continuous Integration/Continuous Deployment (CI/CD) pipeline with GitHub, Docker, Ansible, and other related tools. The purpose of this project is to automate the deployment and management of a simple web application using modern DevOps practices.

### Technologies Used
Git: Version control system for tracking changes in the source code.
GitHub: Hosting service for Git repositories and CI/CD pipelines.
Docker: Platform for building, shipping, and running applications in containers.
Ansible: Automation tool for managing configurations and deployments.
Flask: Lightweight Python web framework for building web applications.
Redis: In-memory data structure store used to keep track of visit counts.
Python: Programming language used for the backend web application.
Docker Compose: Tool for defining and running multi-container Docker applications.
```
CI-CD-example/
├── inventory.ini
├── playbook.yml
└── roles/
    ├── docker/
    │   └── tasks/
    │       └── main.yml
    └── app/
        └── tasks/
            └── main.yml
```
```bash
git clone https://github.com/JUSTRUDYan/CI-CD-example.git
cd CI-CD-example

docker-compose up --build

sudo apt-get install ansible

ansible-playbook ansible/playbook.yml -i ansible/inventory.ini --ask-become-pass
```
# Usage
Accessing the Web Application: Once the Docker containers are up and running, you can access the application in your web browser at http://localhost:5000.

Counter: The web application displays a counter that tracks the number of visits. Each time the page is reloaded, the counter increments by one.

Docker Commands:

Start the application: 
```
docker-compose up
```
Stop the application: 
```
docker-compose down
```
Rebuild the containers: 
```
docker-compose up --build
```

## Disclaimer
This project was developed using Docker Desktop for local development, which provides a convenient environment for managing Docker containers and services on Windows and macOS. As a result, the section of the setup related to downloading and installing Docker Compose is commented out in the configuration. This is because Docker Compose is already included with Docker Desktop, and I did not need to manually install it.

Since Docker Compose is integrated into Docker Desktop, I am not entirely sure if the installation steps for Docker Compose will work flawlessly in all environments, particularly for non-Docker Desktop setups or other operating systems like Linux. Therefore, I recommend verifying whether Docker Compose is available in your environment before proceeding with the setup.

If you are using a different system, or you do not have Docker Desktop installed, please ensure that Docker Compose is installed by following the appropriate installation instructions for your platform.

Let me know if you encounter any issues, and I will do my best to help you resolve them!
