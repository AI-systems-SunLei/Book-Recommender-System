# Book-Recommender-System

<img width="970" height="755" alt="QQ20250731-102931" src="https://github.com/user-attachments/assets/9e19bb8c-54fc-496b-9d52-02f10a8b0c69" />

I have deployed it on AWS. You can open the link to try it out: http://18.232.81.29:8501/

If the page doesn't load or throws an error, please let me know. It's most likely that my AWS account has no funds left.

## Workflow

- config.yaml
- entity
- config/configuration.py
- components
- pipeline
- main.py
- app.py

# How to run?

### STEPS:

Clone the repository

```bash
https://github.com/AI-systems-SunLei/Book-Recommender-System.git
```

### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n books python=3.7.10 -y
```

```bash
conda activate books
```

### STEP 02- install the requirements

```bash
pip install -r requirements.txt
```

Now run,

```bash
streamlit run app.py
```

# Streamlit app Docker Image Deployment

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
docker build -t sunlei416/bookapp:latest .
```

```bash
docker images -a
```

```bash
docker run -d -p 8501:8501 sunlei416/bookapp
```

```bash
docker ps
```

```bash
docker stop container_id
```

```bash
docker rm $(docker ps -a -q)
```

```bash
docker login
```

```bash
docker push sunlei416/bookapp:latest
```

```bash
docker rmi sunlei416/bookapp:latest
```

```bash
docker pull sunlei416/bookapp
```
