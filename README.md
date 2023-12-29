# Streamlit Application

This is a Streamlit application, containerized using Docker. The application is served on port 8502. It uses the pyautogen that allows agents to work together to answer queries, generate code and 
do some general QA about various topics.   

## Prerequisites

- Docker
- Python 3.10

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

## Build the docker image    
```bash
docker build -t streamlit-app .
```
## Run the docker container   
```bash
docker run -p 8502:8502 streamlit-app
```

## Application Health Check

The Docker container includes a health check which uses `curl` to check the main page of the application every 5 minutes. If the main page is not responding, Docker will consider the container to be unhealthy.   

## License

This project is licensed under the MIT License - see the [LICENSE.md](./LICENSE) file for details
