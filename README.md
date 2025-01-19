# ArgoCD GitOps Repository

This repository contains the Helm chart values for managing deployments of the Movie-app application across different environments (`dev`, `staging`, and `prod`) using ArgoCD.

## Structure
```

── environments
    ├── dev
    │   ├── application.yaml
    │   └── values.yaml
    ├── prod
    │   ├── application.yaml
    │   └── values.yaml
    └── staging
        ├── application.yaml
        └── values.yaml
```

## Purpose
- This repository holds the `values.yaml` files for the Helm chart in the [Movie-app repository](https://github.com/OmerSade1/Movie-app).
- Each environment (`dev`, `staging`, and `prod`) has its own set of configurations in the respective `values.yaml` file.
- ArgoCD monitors these files and applies the specified image tags and other configurations to the EKS cluster.

## Key Files
- `application.yaml`: Defines the ArgoCD Application configuration for the environment.
- `values.yaml`: Contains Helm values, including the image tag and other deployment settings.

## Deployment Process
1. Update the `values.yaml` file for the desired environment with the new image tag or other settings.
2. Commit and push the changes to this repository.
3. ArgoCD automatically detects the changes and applies them to the EKS cluster.

## Related Repositories
- [Movie-app Repository](https://github.com/OmerSade1/Movie-app): Contains the Helm chart and application code.


