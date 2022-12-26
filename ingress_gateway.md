# Manually create the namespace

```
kubectl create namespace istio-ingress

```

# Apply sidecar injection via namespace labeling

```
kubectl label namespace istio-ingress istio-injection=enabled

```
# Install ingress

```

helm install istio-ingress istio/gateway -n istio-ingress --wait

```
