# Install EKS

Please follow the prerequisites doc before this.

## Install a EKS cluster with EKSCTL

```
eksctl create cluster --name go-cluster --region us-east-1 
```

## Delete the cluster

```
eksctl delete cluster --name go-cluster --region us-east-1
```