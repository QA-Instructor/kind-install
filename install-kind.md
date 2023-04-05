## Create the KinD Cluster

To create a cluster called `huddle`, navigate into the folder containing the manifest file *kind.yml* and run the following command:


`
kind create cluster --config=kind.yml
`

### Confirm the Cluster was Created

`
kind get clusters
`

### Confirm the kubectl context is set to your new cluster

`
kubectl get nodes
`


This should output:

| NAME |                  STATUS |  ROLES |          AGE |     VERSION |
| --------------------- | ----- | -----| -----| -----|
| huddle-control-plane  | Ready  |  control-plane  | 2m27s  | v1.26.3|
| huddle-worker         | Ready |   `<none>`    |      2m4s   | v1.26.3 |
| huddle-worker2    |     Ready  |  `<none>`     |     2m4s   | v1.26.3 |
| huddle-worker3     |    Ready   | `<none>`      |    2m4s   | v1.26.3 |


---


## Delete the KinD Cluster

To delete a cluster called `huddle`, run the following command:


`
kind delete cluster --name=huddle
`
