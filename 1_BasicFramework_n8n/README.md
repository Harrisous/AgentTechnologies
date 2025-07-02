# Task: build a basic AI agent and get familiar with agent system workflow

## Required Software (first time install):
n8n -- free on github url: https://github.com/n8n-io/n8n <br>
Docker -- to run within isolated environment and config
```
docker volume create n8n_data
docker run -it --rm --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n docker.n8n.io/n8nio/n8n
```
To stop or start n8n service in docker:
```
docker stop n8n
docker start n8n
```

## Model Configuration
### 1. To connect to ollama model (local): 
```
ollama serve
```
Note: <br>
a. If n8n service is running inside Docker and ollama is running on local machine, when configuring n8n, set the Ollama API URL to -- <br>
On Windows/Mac: http://host.docker.internal:11434 <br>
On Linux: http://172.17.0.1:11434 <br><br>
b. If n8n and ollama is running in the same env (both in docker or local host), do not use localhost in API setting, as it may resolve to an IPv6 address (::1), which can cause connection issues if Ollama is only listening on IPv4. Use -- <br>
http://127.0.0.1:11434

### 2. Online AI API
Just create another api key from service provider and paste it. 


