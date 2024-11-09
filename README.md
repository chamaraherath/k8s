# Kubernetes deployment

## Directory structure

```shell
├── application
  └── base
  │   ├── foo.yaml
  │   ├── bar.yaml
  │   └── kustomization.yaml
  └── envs
      ├── dev
      │   ├── foo.yaml            <-- patch
      │   ├── bar.yaml            <-- patch
      │   └── kustomization.yaml
      ├── qa
      │   ├── foo.yaml            <-- patch
      │   ├── bar.yaml            <-- patch
      │   └── kustomization.yaml
      └── prd
          ├── foo.yaml            <-- patch
          ├── bar.yaml            <-- patch
          └── kustomization.yaml
```

With this structure, you can create the YAML files for each deployment as
follows:

```shell
kubectl kustomize application/envs/dev/
kubectl kustomize application/envs/qa/
kubectl kustomize application/envs/prd/
```
