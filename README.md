# Provision an EKS Cluster

This project is based into https://github.com/rodrigofrs13/artigo-aws-eks

## Requirements

- aws cli
- terraform >= 1.3
- helm

## Steps

```
terraform init
```

```
terraform plan 
```

```
terraform apply 
```

```
aws eks --region sa-east-1 update-kubeconfig --name cluster-eks-filipisaci
```

```
kubectl cluster-info 
```

## Install ingress

```
helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
helm install ingress-nginx ingress-nginx/ingress-nginx   --namespace ingress-nginx --create-namespace   --set controller.publishService.enabled=true
```