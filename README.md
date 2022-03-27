<div align="center">
  <p>
    <h1 align="center">
    Docker & Docker Compose
    </h1>
  </p>
</div>

## 🕵️ What's this?
Compose is a tool for defining and running multi-container Docker applications.\
With Compose, you use a YAML file to configure your application’s services.\
Then, with a single command, you create and start all the services from your configuration.

## ✅ Installation
* On Windows/Mac: Install [Docker Desktop](https://www.docker.com/get-started)
* On Linux:
    1. Install Docker Engine: [Debian](https://docs.docker.com/engine/install/debian/), [Ubuntu](https://docs.docker.com/engine/install/ubuntu/)
    2. Install [Docker Compose](https://docs.docker.com/compose/install/)
    ### TL;DR Linux
    ```bash
    # Download Docker Compose
    sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
    
    # Apply executable permissions
    sudo chmod +x /usr/local/bin/docker-compose
    
    # (Optional) install bash completion
    sudo curl \
    -L https://raw.githubusercontent.com/docker/compose/1.29.2/contrib/completion/bash/docker-compose \
    -o /etc/bash_completion.d/docker-compose
    
    # Test installation
    docker-compose --version
    ```

## 🛠️ How to setup?
1. Open terminal and navigate to local copy of this repo.
2. Run command: 
    ```bash 
    docker-compose up -d
    docker exec -it api cp .env.example .env
    docker exec -it api php artisan key:generate
    docker exec -it api composer update
    docker exec -it api php artisan migrate
    ```

## 💡 Useful commands
```bash
# List running containers
docker-compose ps

# List available images
docker-compose images

# Connect to running condainer
docker exec <SERVICE-NAME> bash

# Start environment
docker-compose up

# Restart container
docker-compose restart <SERVICE-NAME>

# Stop running container
docker-compose stop <SERVICE-NAME>

# Stop and remove environment
docker-compose down
```

## 📜 References
[Docker Compose CLI Reference](https://docs.docker.com/compose/reference/) \
[Docker Compose File Reference](https://docs.docker.com/compose/compose-file/compose-file-v3/)

