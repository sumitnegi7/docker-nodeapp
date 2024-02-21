🐳 **Docker Commands Cheat Sheet** 🐳

- **Build an image:**  
  `docker image build -t username/demoapp:1.0 .`  
  This command builds a Docker image from the current directory (`.`) and tags it as `username/demoapp` with version `1.0`.

- **Run a container:**  
  `docker run -p 5000:8080 nodeapp`  
  This command runs a Docker container named `nodeapp` and maps port `5000` on the host to port `8080` on the container.

- **Create a volume:**  
  `docker volume create shared-stuff`  
  This command creates a Docker volume named `shared-stuff`, which can be used to share data between containers or persist data.

- **Mount a volume:**  
  `docker run --mount source=shared-stuff,target=/stuff`  
  This command runs a new container and mounts the `shared-stuff` volume to the `/stuff` directory in the container.

- **Run a container with specific settings:**  
  `docker run -it --rm --name nodehello -p 3000:3000 nodehello`  
  This command runs a new container named `nodehello` with an interactive terminal (`-it`), removes the container when it exits (`--rm`), and maps port `3000` on the host to port `3000` on the container.

- **Build services:**  
  `docker-compose build`  
  This command builds the services defined in your `docker-compose.yml` file. It reads the `Dockerfile` in each service's build context and creates an image for each service.

- **Start services:**  
  `docker-compose up`  
  This command starts the services defined in your `docker-compose.yml` file. It creates and starts containers for each service, as well as any volumes and networks defined in the `docker-compose.yml`.

- **Rebuild and start services:**  
  `docker-compose up --build`  
  This command is similar to `docker compose up`, but it also rebuilds the images before starting the services. Use this when you've made changes to your `Dockerfile` or any files the `Dockerfile` depends on, and you want to ensure those changes are included in the image before starting the services.
