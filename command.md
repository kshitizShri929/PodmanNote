Here’s a **Podman Command Cheat Sheet** covering container, image, network, volume, and system management.  

---

## 🔹 **Basic Podman Commands**
```sh
podman version             # Check Podman version
podman info                # Show system-wide information
podman help                # Get help for Podman commands
podman system df           # Show disk usage by images, containers, and volumes
```

---

## 🔹 **Container Management**
```sh
podman ps                  # List running containers
podman ps -a               # List all containers (including stopped)
podman run -it <image>     # Run a container interactively
podman run -d <image>      # Run a container in detached mode
podman start <container>   # Start a stopped container
podman stop <container>    # Stop a running container
podman restart <container> # Restart a container
podman kill <container>    # Forcefully stop a container
podman rm <container>      # Remove a container
podman logs <container>    # Show logs of a container
podman top <container>     # Show running processes in a container
podman stats               # Show real-time resource usage of running containers
podman inspect <container> # Get detailed information about a container
podman exec -it <container> bash  # Execute a command in a running container
```

---

## 🔹 **Image Management**
```sh
podman images              # List all images
podman pull <image>        # Download an image from a registry
podman push <image>        # Upload an image to a registry
podman rmi <image>         # Remove an image
podman inspect <image>     # Get details of an image
podman tag <image> <new_tag>  # Tag an image
podman history <image>     # Show image history
```

---

## 🔹 **Building Images**
```sh
podman build -t <tag> .    # Build an image from a Dockerfile
podman commit <container> <new_image>  # Create an image from a container
```

---

## 🔹 **Network Management**
```sh
podman network ls          # List all networks
podman network inspect <network>  # Inspect network details
podman network create <network>   # Create a new network
podman network rm <network>       # Remove a network
podman network connect <network> <container>  # Connect a container to a network
podman network disconnect <network> <container>  # Disconnect a container from a network
podman run --network=<network> -d <image>  # Run a container in a specific network
```

---

## 🔹 **Volume Management**
```sh
podman volume ls           # List all volumes
podman volume create <volume>  # Create a volume
podman volume inspect <volume> # Inspect a volume
podman volume rm <volume>       # Remove a volume
podman run -v <volume>:/path/in/container <image>  # Attach a volume to a container
```

---

## 🔹 **Pod Management**
```sh
podman pod create --name <pod_name>  # Create a new pod
podman pod ls            # List all pods
podman pod start <pod>   # Start a pod
podman pod stop <pod>    # Stop a pod
podman pod rm <pod>      # Remove a pod
podman pod inspect <pod> # Get details of a pod
podman pod ps            # List containers inside a pod
```

---

## 🔹 **System and Troubleshooting**
```sh
podman system prune        # Remove unused images, containers, and volumes
podman system reset        # Reset Podman to default settings
podman events              # Show real-time events
podman healthcheck run <container>  # Run a health check on a container
podman checkpoint <container>  # Save a container’s state
podman restore <container>  # Restore a container from a checkpoint
```

---

### 🎯 **Example: Run a Web Server in Podman**
```sh
podman run -d -p 8080:80 nginx
```
This runs an **nginx** web server, mapping host port **8080** to container port **80**.

---

Would you like me to add specific **examples or explanations**? 🚀
