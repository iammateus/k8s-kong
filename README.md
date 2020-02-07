# K8sKong

This project contains a set of Kubernetes manifests to serve as an example of kubernetes-ingress-controller usage to manage microservices.

## Installs Kong Ingress Controller

```
curl -sL https://bit.ly/k4k8s | kubectl create -f -
```

### Creates an echo service for testing

```
kubectl apply -f https://bit.ly/echo-service
```

### Creates PROXY_IP environment variable with the cluter ip

```
export PROXY_IP=$(minikube service -n kong kong-proxy --url | head -1)
```

### Prints cluter ip

```
echo $PROXY_IP
```

### Applies all manifests

```
kubectl apply -f kong-plugin.yaml
```

```
kubectl apply -f ingress.yaml
```

```
kubectl apply -f kong-consumer.yaml
```

```
kubectl apply -f kong-credential.yaml
```
