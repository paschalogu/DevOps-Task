# DevOps-Task

DevOps Test:
1. Create a helm chart.
2. Your helm chart should deploy two application containers: a frontend app and it’s backend into your Kubernetes cluster.
3. configure Ingress to access your applications.

## Creating an application with Helm Chart:

### My setup:
- Ubuntu Linux Distribution (Virtualized on VMware workstation)
- Docker 
- Locally installed Kubernetes cluster - Microk8s
- Kubernetes command line tool - kubectl
- Helm Installed
- A sample application: Voting App with front end and backend that shows result on the results page. The voting application only accepts one vote per client browser. It does not register additional votes if a vote has already been submitted from a client.

### App Architecture

![App Architecture](https://github.com/paschalogu/DevOps-Task/blob/main/architecture-votingapp.png?raw=true)

To run the app locally run the below command:

### Clone the repository:

```
git clone https://github.com/paschalogu/DevOps-Task.git
```

navigate inside the repository 

```
cd DevOps-Task
tree .
```

```
helm lint votingapp
```

### To install and run the deployment run the command bellow

```
helm install myvotingapp votingapp
```

### Verify the helm install

```
helm list -a
```

```
kubectl get all
```

### To Delete Helm release

```
helm delete myvotingapp
````
