# 2026-08-25

Quick notes from this sandbox session:

- Deployed a local kind cluster for testing kube-prometheus-stack.
- Need to verify `thanos` sidecar uploads blocks to the object store.
- Useful command:
  ```bash
  kubectl -n monitoring port-forward svc/thanos-query-frontend 9090:9090
  ```
- TODO: add a kustomize overlay to customise alertmanager routes.
