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

- Kubernetes is made of control plane nodes (aka cp nodes) and worker nodes, once called minions
- K8 exposes an API by which you can commincate with the server via a local client and kubectl commands. You can also create your own client with curl commands
- each node runs two process:
1. kubelet -> systemd command: received requests to run the containers and manage resources on local node
2. kube-proxy -> creates/manages networking rules to expose teh container on the network to other containers (other services) or the outside world

- the objects and sate of the cluster are stored in etcd: https://etcd.io

**Pod**: Pod consists of one or more containers which share an IP address, access to storage and namespace. Typically, one container in a Pod runs an application, while other containers support the primary application.

**Operators**: manage pod orchestration through watch loops. Each operator interrorgates the kube-apiserver for a specific object state and modyifies the object until it matches the desired state.

**Deployment** default operator for containers. Manages Replicasets which are operators to create/terminate pods according to podSpec.

- use labels to manage pods easier without having to know individual container names or UIDs

- use annotations in metadata to hold info that will be used by the containers or 3rd parties

- Our labs will focus on the use of kubeadm and kubectl, which are very powerful and complex tools

- **Helm**: an easy tool for using Kubernetes, to search for and install software using charts
