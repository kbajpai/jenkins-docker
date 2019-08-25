# jenkins-docker
Docker image for jenkins with docker support    

### Build Image
`
docker image build -t dev/jenkins:latest .
`

### Run Jenkins Container
`
docker run -d --name jenkins_latest \
	-p 8085:8080 -p 50000:50000 \
	-v /home/jenkins_home:/var/jenkins_home \
	-v /var/run/docker.sock:/var/run/docker.sock \
	dev/jenkins:latest
`
