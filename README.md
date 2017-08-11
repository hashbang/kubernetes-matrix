## Try it out locally

```
# Start minikube
minikube start 
#--container-runtime=rkt

# https://github.com/kubernetes/minikube/blob/master/docs/host_folder_mount.md
# minikube mount --uid 1000 --gid 1000 .:/exp &

# https://github.com/kubernetes/minikube/blob/master/docs/reusing_the_docker_daemon.md
eval $(minikube docker-env)

source <(kubectl completion bash)

# To run a misc docker container
# kubectl run --image=silviof/docker-matrix matrix

# To deploy matrix
kubectl create -f matrix.yaml

# To deploy changes:
kubectl replace -f matrix.yaml --force
```
