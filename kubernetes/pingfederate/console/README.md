## Overview

Start a PingFederate admin console as part of a cluster

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
kubectl logs -f pod/pf-cluster-console-id
```

## get admin console

```
kubectl port-forward pod/pf-cluster-console-id 9999:9999
```

Point web browser to https://localhost:9999/pingfederate/app

administrator / 2FederateM0re

## clean everything up

Be careful deleting the devops-secret, as it may be required for other items your cluster.

```
kubectl delete deployment.apps/pf-cluster-console
kubectl delete configmap console-variables
```
