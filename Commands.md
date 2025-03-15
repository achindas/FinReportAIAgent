# Streamlit app Docker Image

## 1. Login with your AWS console and launch an EC2 instance
## 2. Run the following commands

Note: Do the port mapping to this port:- 8501

```bash
sudo apt-get update -y

sudo apt-get upgrade

#Install Docker

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker
```

```bash
git clone "your-project"
```

```bash
# Build or update a docker image based on Dockerfile specs
docker build -t achindas/fin-report-ai-agent:latest . 
```

```bash
# List all images
docker images -a  
```

```bash
# Run an image as container on port 8501 by mapping local ./coding folder to container's /coding folder
docker run -d -p 8501:8501 -v $(pwd)/coding:/coding achindas/fin-report-ai-agent 
```

```bash
# List all running containers
docker ps  
```

```bash
# Stop a container by ID
docker stop container_id
```

```bash
# Remove all running and stopped containers
docker rm $(docker ps -a -q)
```

```bash
# Login to remote Docker Hub
docker login 
```

```bash
# Push image to Docker Hub
docker push achindas/fin-report-ai-agent:latest 
```

```bash
# Remove image from local
docker rmi achindas/fin-report-ai-agent:latest
```

```bash
# Pull image to current environment
docker pull achindas/fin-report-ai-agent:latest
```

```bash
# Logout of remote Docker Hub
docker logout
```






