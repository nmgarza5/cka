## Basics of Kubernetes

Software designed for automating deployment scaling and management of containerized applications

**Components of Kubernetes**
- solves the issue of high web traffic by deploying a large number of small servers or web services
- the server and client sides of the application are designed to expect many possible agents are avialable to respond to a request

**Challenges**
- docker containers have made it easy to use k8s but also had its challenges
- need a cluster of machines to run your containers
- need a system to launch your containers -> watch over them when they fail and replace as required
- autoscaling is important
- require flexible, scalable, and easy-to-use network and storage
- as containers are launched on a worker nodes, the network must join this container to the other containers while keeping traffic secure

**Kubernetes Architecture**
![Kubernetes-arch-tecture-diagram](j0i2uejk3hr5-Kubernetes_Architecture.png)
