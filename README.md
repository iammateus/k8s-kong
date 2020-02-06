# K8sKong

## Installs Kong Ingress Controller:

```
curl -sL https://bit.ly/k4k8s | kubectl create -f -
```

## Returns Kong url:

```
export PROXY_IP=$(minikube service -n kong kong-proxy --url | head -1)
```

```
echo $PROXY_IP
```