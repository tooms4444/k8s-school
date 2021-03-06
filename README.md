# k8s-school

# Course

All materials are [here](https://drive.google.com/open?id=0B-VJpOQeezDjZktuTnlEMEpGMUU)

# Exercices

## Pre-requisites

### Set up local machine

Depending on your linux distribution version, you might have to upgrade to docker-ce:
https://docs.docker.com/install/linux/docker-ce/ubuntu/#install-docker-ce-1

```shell
# Install dind cluster
wget https://cdn.rawgit.com/Mirantis/kubeadm-dind-cluster/master/fixed/dind-cluster-v1.9.sh

./dind-cluster-v1.9.sh up

# Get configuration file from dind cluster
docker cp kube-master:/etc/kubernetes/admin.conf  ~/src/k8s-school/dot-kube/dindconfig
ln -sf ~/src/k8s-school/dot-kube/dindconfig ~/src/k8s-school/dot-kube/config

# Run kubectl client inside container and play with k8s
./run-kubectl.sh
```

## Play with dashboard

http://localhost:8080/api/v1/namespaces/kube-system/services/kubernetes-dashboard:/proxy

## Play with examples

## Install 2 example apps
https://github.com/kubernetes/examples/blob/master/README.md

## Install Prometheus

See [here](./README.monitor.md)
