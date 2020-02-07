# K8sKong

## Installs Kong Ingress Controller:

```
curl -sL https://bit.ly/k4k8s | kubectl create -f -
```

## Creates an echo service for testing

```
kubectl apply -f https://bit.ly/echo-service
```

## Creates environment variable PROXY_IP with the cluter ip

```
export PROXY_IP=$(minikube service -n kong kong-proxy --url | head -1)
```

## Returns PROXY_IP

```
echo $PROXY_IP
```