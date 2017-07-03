# Jenkins swarm slave


## Running

To run this container in your computer, you'll need a running Jenkins Docker container. The commands bellow will do the job:

```bash
docker run -d --name jenkins -p 8080:8080 -p 50000:50000 sivakumar/jenkins-swarm
docker run -d --name jenkins-slave-01 --link jenkins:jenkins sivakumar/jenkins-swarm-slave
```

# Building

```bash
docker build -t <username>/jenkins-swarm-slave .
```
