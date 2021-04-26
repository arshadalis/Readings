# K8S Architecture


#### Kubelet
Simple Container running system which watches particular directory to run pods on itself. It registers to API server.
It has container runtime like docker. 


#### API Server
All the state of the cluster is stored in the database called etcd. etcd is implementation of raft (https://github.com/etcd-io/etcd).
etcd holds all the information like nodes, which pods should be running etc.

API server is the only component of k8s which talks to etcd.

Kubelets registers themselves to API server. API server then knows the no of nodes it has. 

#### Scheduler

