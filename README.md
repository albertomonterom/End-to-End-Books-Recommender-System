# End-to-End-Books-Recommender-System
End-to-end book recommendation system built with collaborative filtering

## Workflow

- config.yaml
- entity
- config/configuration.py
- components
- pipeline
- main.py
- app.py

# How to run?

### 1. Clone the Repository
```bash
git clone https://github.com/albertomonterom/End-to-End-Books-Recommender-System.git
cd End-to-End-Books-Recommender-System
```

### 2. Create a virtual environment
```bash
python -m venv books
```

Activate it

```bash
source books/bin/activate   # Linux/Mac
books\Scripts\activate      # Windows
```

### 3. Install Requirements
```bash
pip install -r requirements.txt
```

Now run,
```bash
streamlit run app.py
```


# Streamlit App Deployment with Docker on AWS EC2

## 1. Login with your AWS console and launch an EC2 instance

## 2. Install Docker on the Instance

#### Run the following commands:

```bash
sudo apt-get update -y
sudo apt-get upgrade
```

Install Docker:
```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
```

Give the ubuntu user Docker permissions:
```bash
sudo usermod -aG docker ubuntu
newgrp docker
```

## 3. Clone Your Project from GitHub

```bash
git clone "your-project"
cd <your_repo>
```

## 4. Build the Docker Image

```bash
docker build -t albertomonterom/bookapp:latest .
```

Check the built image:
```bash
docker images -a  
```

## 5. Run the Container

```bash
docker run -d -p 8501:8501 albertomonterom/bookapp
```

See running containers:
```bash
docker ps  
```

Open your app in the browser:
```bash
docker run -d -p 8501:8501 albertomonterom/bookapp
```

## 6. Stop and Clean Up Containers

Stop a container:
```bash
docker stop <container_id>
```

Remove all stopped containers:
```bash
docker rm $(docker ps -a -q)
```

## 7. Push Image to Docker Hub

Login to Docker Hub:
```bash
docker login 
```

Push your image:
```bash
docker push albertomonterom/bookapp:latest
```

```bash
docker rmi albertomonterom/bookapp:latest
```

## 8. Pull the Image from Docker Hub

On any machine with Docker installed:
```bash
docker pull albertomonterom/bookapp
docker run -d -p 8501:8501 albertomonterom/bookapp
```