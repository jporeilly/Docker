## <font color='red'> Docker </font>
Docker is a tool designed to make it easier to create, deploy, and run applications by using Containers. Containers allow a developer to package up an application with all of the parts it needs, such as libraries and other dependencies, and deploy it as one package. 

Docker CE has already been installed and configured.

---

### <font color='red'> 1.1 Docker </font>
check Docker status:
```
systemctl status Docker
```
check Docker:
```
docker info
```
list Containers:
```
docker ps
```
you may find there's a Portainer Container running..!  

For further information:  

> Docker docs: https://docs.docker.com/

---
  

This section contains some tools you may find useful.

### <font color='red'> Portainer </font>
Portainer is an open-source toolset that allows you to easily build and manage Containers in Docker, Swarm, Kubernetes and Azure ACI.

Use the following Docker commands to deploy the Portainer Server.

create a volume:
```
docker volume create portainer_data
```
pull down the container:
```
 docker run -d -p 8000:8000 -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce
```

> To access Portainer: http://0.0.0.0:9000/#!/auth  

    * user: admin  
    * password: portainer

For further information:  

> Portainer docs: https://documentation.portainer.io/

---

### <font color='red'> Weave Scope </font>
Weave Scope automatically detects processes, containers, hosts.

download Weave Scope:
```
sudo curl -L git.io/scope -o /usr/local/bin/scope
```
change permissions:
```
sudo chmod a+x /usr/local/bin/scope
```
launch scope:
```
scope launch
```

> view in browser: http://<vm-IP address>:4040 

---