## CatSet

This is a reimplementation of StatefulSet (except for rolling updates) as a LambdaController.

For this example, you need a cluster with a default storage class and a dynamic provisioner.

### Prerequisites

* [Install Metacontroller](https://github.com/GoogleCloudPlatform/kube-metacontroller#install)

### Deploy the controller

```sh
kubectl create configmap catset-controller -n metacontroller --from-file=sync.js
kubectl create -f catset-controller.yaml
```

### Create a CatSet

```sh
kubectl create -f my-catset.yaml
```