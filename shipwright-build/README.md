docker.io/paketobuildpacks/builderBUILDER_CONTAINER_IMAGEBUILDER_CONTAINER_IMAGE# shipwright-build

A Helm chart for Shipwright Build on Kubernetes

## Requirements

Kubernetes: `>=v1.21.0-0`

## Verify installation

```
kubectl get po -n shipwright-build
```

## Uninstall the Chart

To uninstall/delete the `shipwright-build` release:
```
helm uninstall shipwright-build -n shipwright-build
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| kubernetesClusterDomain | string | `"cluster.local"` |  |
| shipwrightBuildController.replicas | int | `1` |  |
| shipwrightBuildController.shipwrightBuild.BUNDLE_CONTAINER_IMAGE.repository | string | `"ghcr.io/shipwright-io/build/bundle"` |  |
| shipwrightBuildController.shipwrightBuild.BUNDLE_CONTAINER_IMAGE.tag | string | `"v0.10.0"` |  |
| shipwrightBuildController.shipwrightBuild.GIT_CONTAINER_IMAGE.repository | string | `"ghcr.io/shipwright-io/build/git"` |  |
| shipwrightBuildController.shipwrightBuild.GIT_CONTAINER_IMAGE.tag | string | `"v0.10.0"` |  |
| shipwrightBuildController.shipwrightBuild.MUTATE_IMAGE_CONTAINER_IMAGE.repository | string | `"ghcr.io/shipwright-io/build/mutate-image"` |  |
| shipwrightBuildController.shipwrightBuild.MUTATE_IMAGE_CONTAINER_IMAGE.tag | string | `"v0.10.0"` |  |
| shipwrightBuildController.shipwrightBuild.WAITER_CONTAINER_IMAGE.repository | string | `"ghcr.io/shipwright-io/build/waiter"` |  |
| shipwrightBuildController.shipwrightBuild.WAITER_CONTAINER_IMAGE.tag | string | `"v0.10.0"` |  |
| shipwrightBuildController.shipwrightBuild.image.repository | string | `"ghcr.io/shipwright-io/build/shipwright-build-controller"` |  |
| shipwrightBuildController.shipwrightBuild.image.tag | string | `"v0.10.0"` |  |
| shipwrightBuildController.shipwrightBuild.BUILDER_CONTAINER_IMAGE.repository | string | `docker.io/paketobuildpacks/builder` |  |
| shipwrightBuildController.shipwrightBuild.BUILDER_CONTAINER_IMAGE.tag | string | `full` |  |