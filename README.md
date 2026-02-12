# argo-test-app — kustomize overlays

This repo contains Kubernetes manifests and kustomize overlays for three environments: `dev`, `staging`, and `prod`.

Quick apply examples:

Apply dev:
```bash
kubectl apply -k kustomize/overlays/dev
```

Apply staging:
```bash
kubectl apply -k kustomize/overlays/staging
```

Apply prod:
```bash
kubectl apply -k kustomize/overlays/prod
```

Then open the service (NodePort 30080):

If cluster exposes node on localhost (Docker Desktop / minikube tunnel):
```bash
open http://localhost:30080
```

Or with minikube:
```bash
minikube service argo-test-service -n argo-test --url
```
# argo-test-app