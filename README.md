# myCode

# Docker command to create image
docker build -t docker-mycode .

# Docker command to create container
docker run -d -p 27017:27017 -p 8080:8080 --name myCode docker-mycode

# Docker clean up commands
docker rm -f $(docker ps -a -q)
docker rmi $(docker images -q)

# Docker command to get container info
docker exec myCode cat /etc/hosts

#Install kubectl
docker build -t gcr.io/barclays-poc/barclays-mycode .
