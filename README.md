# K8S-MANIFEST

Management repository to store and maintain Kubernetes related manifests for Kubernetes clusters.

## Getting Started

The directory structure is divided into the following sections:

* [bootstrap](./bootstrap): This section contains the bootstrap configuration for the Kubernetes cluster, currently only ArgoCD considered as a bootstrap component.
* [cluster-components](./cluster-components): Stores all cluster components that categorized into different environments such as development, [staging](./cluster-components/staging), and production of Kubernetes clusters. In this directory, we follow [App of Apps](https://argo-cd.readthedocs.io/en/stable/operator-manual/cluster-bootstrapping/#app-of-apps-pattern) pattern, which we store list of ArgoCD applications that considered as cluster components per-cluster basis. The cluster-components application itself, can be seen in [here](./bootstrap/argocd/overlays/staging/applications/cluster-components.yaml).
* [resources](./resources): Stores all resources to which being used or deployed within the cluster-components.
