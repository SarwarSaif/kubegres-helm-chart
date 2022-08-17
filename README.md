# kubegres-helm-chart
This is a helm chart implementation for the kubegres.

## Installation
1. Create the crd
```
k apply -f kubegres-crd/custom-resource-kubegres.yaml -n kubegres
```
2. Helm Installation
```
helm upgrade --install kubegres-helm-test kubegres-postgres/ -n kubegres
```
3. Uninstallation
```
helm delete kubegres-helm-test -n kubegres
```