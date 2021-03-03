# Coredns Helm Chart repository

## Kubernetes

This is a basic repository for *Coredns* helm charts.

### Helm Chart

This repository provides helm chart repo.

Helm `v2`
```bash
helm repo add coredns https://coredns.github.io/helm
helm install coredns/
```

Helm `v3`
```bash
helm helm repo add coredns https://coredns.github.io/helm
install coredns coredns/coredns --version 1.14.1
```
