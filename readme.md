# Install with Docker

### This Dockerfile:

- Uses the official Python 3.11 image from Docker Hub.
- Sets the working directory to /app.
- Copies the local directory contents into the container at /app.
- Installs the necessary dependencies (you might need to have a requirements.txt file with your dependencies).
- Exposes port 8000 (the default FastAPI port).
- Defines an environment variable (you can modify this if needed).
- Finally, runs the FastAPI application using uvicorn.

#### Build Image & Run Container

- Build the Docker image using the following command in the terminal (make sure you are in the directory where your Dockerfile is):

```bash
docker build -t fastapi-app .
```

Replace fastapi-app with your desired image name.

- Run the Docker container:

```bash
docker run -p 8000:8000 fastapi-app
```

Now, your FastAPI application should be accessible at http://localhost. Adjust the port mapping (-p flag) if needed.

Note: Make sure to adapt the version numbers and configurations based on your specific needs and environment.
