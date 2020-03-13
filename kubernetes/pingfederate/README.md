## Overview

Start a single PingFederate instance in Kubernetes, with both the admin console and runtime engine.

## devops-secret

```
./devops-secret
```

## variables

```
kubectl apply -f variables.yaml
```

## deployment

```
kubectl apply -f deployment.yaml
```

## see deployment

```
kubectl get all
```

## pingfederate logfile

```
kubectl logs -f pod/pingfederate-pod-id
```

## get admin console

```
kubectl port-forward pod/pingfederate-pod-id 9999:9999
```

Point web browser to https://localhost:9999/pingfederate/app

administrator / 2FederateM0re

## clean everything up

```
kubectl delete deployment.apps/pingfederate
kubectl delete service/pingfederate
kubectl delete secret devops-secret
kubectl delete configmap standalone-variables
```
