This repository hosts the [Helm Chart component](https://github.com/rancher/local-path-provisioner) from `rancher/local-path-provisioner` for usage in a cluster.

# local-path-provisioner

> Local Path Provisioner provides a way for the Kubernetes users to utilize the local storage in each node. Based on the user configuration, the Local Path Provisioner will create hostPath based persistent volume on the node automatically. It utilizes the features introduced by Kubernetes Local Persistent Volume feature, but make it a simpler solution than the built-in local volume feature in Kubernetes.

## Helm

*A hosted Helm chart* is available. Use the following commands to use it. https://tablecheck-labs.github.io/local-storage-provisioner/

```
helm repo add tablecheck-local-provisioner https://tablecheck-labs.github.io/local-storage-provisioner/
helm upgrade --install tablecheck-local-provisioner tablecheck-local-provisioner/local-storage-provisioner
```

For local installations:

```
helm upgrade --install --namespace=kube-system local-storage-provisioner ./helm/local-path-provisioner
```

## Relation to sig-storage-local-static-provisioner
 - eks-nvme-ssd-provisioner creates disks from block storage
 - This version of the local-storage-provisioner creates hostPath based persistent volume on the node automatically. Thanks Rancher!

If you want the NVMe provisioner, it's available here: https://github.com/TableCheck-Labs/eks-nvme-ssd-provisioner
