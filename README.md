# kubegres-helm-chart
This is a helm chart implementation for the kubegres.

## Installation
1. Create the crd
```
k apply -f kubegres-crd/custom-resource-kubegres.yaml -n kubegres
```
2. Helm Installation
```
helm upgrade --install kubegres-helm-test kubegres-helm-chart/ -n kubegres
```
3. Uninstallation
```
helm delete kubegres-helm-test -n kubegres

k delete cm base-kubegres-config
k delete cm d5ccd92e.reactive-tech.io

base-kubegres-config        7      159m
d5ccd92e.reactive-tech.io   0      159m
kube-root-ca.crt            1      170m
```

## Kubegres Documentation
https://www.kubegres.io/doc/properties-explained.html
https://www.kubegres.io/doc/override-default-configs.html
