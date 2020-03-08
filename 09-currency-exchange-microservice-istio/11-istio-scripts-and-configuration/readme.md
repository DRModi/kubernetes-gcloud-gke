# Setting up istio

```
### Connect to kubernetes cluster: on google cloud
gcloud container clusters get-credentials drm-cluster-istio --zone us-central1-a --project drm-gke-crash-course

### Create namespace for istio
kubectl create namespace istio-system

#### Download istio and apply
curl -L https://git.io/getLatestIstio | ISTIO_VERSION=1.2.2 sh -
cd istio-1.2.2 
for i in install/kubernetes/helm/istio-init/files/crd*yaml; do kubectl apply -f $i; done

### Install pre-created templates - helm
helm template install/kubernetes/helm/istio --name istio --set global.mtls.enabled=false --set tracing.enabled=true --set 
kiali.enabled=true --set grafana.enabled=true --namespace istio-system > istio.yaml

###Create yml file for istio
kubectl apply -f istio.yaml


kubectl label namespace default istio-injection=enabled
```

# Using Kiali

- http://localhost:20001

```
kubectl port-forward \
    $(kubectl get pod -n istio-system -l app=kiali \
    -o jsonpath='{.items[0].metadata.name}') \
    -n istio-system 20001
```
Create a secret
```
kubectl get secret -n istio-system kiali
kubectl create secret generic kiali -n istio-system --from-literal=username=admin --from-literal=passphrase=admin
```

# Using Graphana to see prometheus metrics
- http://localhost:3000

```
kubectl -n istio-system port-forward \
    $(kubectl -n istio-system get pod -l app=grafana \
    -o jsonpath='{.items[0].metadata.name}') 3000
```

# Using Jaeger

http://localhost:16686

```
kubectl port-forward -n istio-system \
    $(kubectl get pod -n istio-system -l app=jaeger \
    -o jsonpath='{.items[0].metadata.name}') 16686
```