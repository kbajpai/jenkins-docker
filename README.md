# jenkins-docker
Docker image for jenkins with docker support    
##Note-  Chnage the line `docker-ce=17.12.1~ce` depending on ther version of docker client you need to use.

### Build Image
`
docker image build -t dev/jenkins:latest .
`

### Run Jenkins Container
`
docker run --name jenkins_latest -d \
	-v jenkins_home:/var/jenkins_home 
	-v /var/run/docker.sock:/var/run/docker.sock docker \
	-p 8085:8080 -p 50000:50000 \
	dev/jenkins:latest
`
