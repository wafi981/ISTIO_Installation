# Add the istio Helm repo to your Helm installation and update Helm
```
helm repo add istio https://istio-release.storage.googleapis.com/charts
helm repo update

```


# Manually create the namespace
```

kubectl create namespace istio-system

```


# install the base (CRDs)
```

helm install istio-base istio/base -n istio-system

```


# install IstioD (the control plane)
```

helm install istiod istio/istiod -n istio-system --wait

```

# Note:


Just add ``` kubeconfig ``` tag to specify which cluster you are installing the chart for

For example 

```

helm install xyz...  --kubeconfig /home/ubuntu/work/kind/.kind2/config

```

