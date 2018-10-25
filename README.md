Docker image for build systems using Kustomize and kubectl in Google Cloud Builder.

# Usage

Add the following item to your `cloudbuild.yaml`:

```yaml
  - name: 'marc/kustomize-docker'
    entrypoint: 'sh'
    args:
      - '-c'
      - |
        kustomize build /workspace/kustomize/overlays/production > /workspace/gitops-deploy/api/api.yaml
```