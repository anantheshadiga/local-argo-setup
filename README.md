This repo have receipes to run argo on local. 

### Prerequisite to run argo in mac
Install kind
```bash
brew install kind
kind create cluster
```
### Install argo without https
```bash
kubectl create ns argo
brew install argoproj/tap/argo
kubectl apply -n argo -f https://raw.githubusercontent.com/anantheshadiga/local-argo-setup/main/quick-start-postgres.yaml
```

- Port forward
```bash
kubectl -n argo port-forward deployment/argo-server 2746:2746
```

Check argo running on http://localhost:2746