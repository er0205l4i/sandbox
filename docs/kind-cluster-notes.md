# Kind Cluster Notes

Quick reference for spinning up a local Kubernetes cluster with kind.

## Create cluster

```bash
kind create cluster --name sandbox --config kind-config.yaml
```

## Common commands

```bash
kubectl cluster-info --context kind-sandbox
kubectl get nodes -o wide
kind export logs --name sandbox ./logs
```

## Delete cluster

```bash
kind delete cluster --name sandbox
```

## Port forwarding

```bash
kubectl port-forward -n observability svc/prometheus-operated 9090:9090
```

Remember to check `kubectl get events --sort-by='.lastTimestamp'` when debugging.
