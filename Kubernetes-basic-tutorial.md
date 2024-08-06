# Instructions for playing with Kubernetes in CloudLab using HotelReservation

This tutorial familiarizes participants with basic Kubernetes Operations, such as setting resource allocations for containers and scaling up/down a pod.  

## Start  the cluster 

1. Choose the deathstarbench-k8s-setup profile, which is part of the Tracing-Pythia project.
2. Enter the profile configuration options
     1. DeathStarBench in this profile is pre-built to work with Intel Machines, so choose machines w/Intel CPUs.  Good choices include c6525-25g and c6525-100g in CloudLab Utah.  
     2. You may or may not wish to increase the number of nodes.
     3. You can leave the rest of the options as default.
     4.  Read the README for deathstarbench-k8s-setup profile, which provides detailed information about the profile and how deathstarbench is configured.
     5. You will receive two emails, one indicating the clsuter is setting up and another indicating the cluster is ready.  Wait for the latter email before trying to use the cluster.  It can take up to 15 min. 
     6.  Once you receive the email, HotelReservation should be running within Kubernetes 

## Default configuration
1. (This should be in deathstarbench-k8s-setup-profile)

## Explore Kubernetes Commands

`kubectl` is the command for interfacing with and managing kubernetes clusters.  This [website](https://spacelift.io/blog/kubernetes-cheat-sheet) and this [one] (https://kubernetes.io/docs/concepts/workloads/controllers/deployment/)  provide a nice overview of this command.  Please read through them.  

#### Deployments
Deployments allows users to configure Kubrnetes Pods and Replicas.  
1. **List deployments**: `kubectl get deployments` lists all deployed services
   *`kubectl get deployments` lists all services deployed for HotelReservation as well as kubernetes services.  
3. **Get deployment info**: `kubectl describe deployment/<name>` describes details of deployments
   * 'kubectl get deployment/frontend` shows resource allocation and status informaton for the Frontend.
```
      Name:                   frontend
Namespace:              default
CreationTimestamp:      Tue, 06 Aug 2024 12:47:24 -0600
Labels:                 io.kompose.service=frontend
Annotations:            deployment.kubernetes.io/revision: 1
                        kompose.cmd: kompose convert
                        kompose.version: 1.22.0 (955b78124)
Selector:               io.kompose.service=frontend
Replicas:               1 desired | 1 updated | 1 total | 1 available | 0 unavailable
StrategyType:           RollingUpdate
MinReadySeconds:        0
RollingUpdateStrategy:  25% max unavailable, 25% max surge
Pod Template:
  Labels:       io.kompose.service=frontend
  Annotations:  kompose.cmd: kompose convert
                kompose.version: 1.22.0 (955b78124)
                sidecar.istio.io/statsInclusionPrefixes:
                  cluster.outbound,cluster_manager,listener_manager,http_mixer_filter,tcp_mixer_filter,server,cluster.xds-grp,listener,connection_manager
                sidecar.istio.io/statsInclusionRegexps: http.*
  Containers:
   hotel-reserv-frontend:
    Image:      deathstarbench/hotel-reservation:latest
    Port:       5000/TCP
    Host Port:  0/TCP
    Command:
      frontend
    Limits:
      cpu:  1
    Requests:
      cpu:        100m
    Environment:  <none>
    Mounts:       <none>
  Volumes:        <none>
Conditions:
  Type           Status  Reason
  ----           ------  ------
  Available      True    MinimumReplicasAvailable
  Progressing    True    NewReplicaSetAvailable
OldReplicaSets:  <none>
NewReplicaSet:   frontend-bd4f9cf9f (1/1 replicas created)
Events:          <none>
rajas@node-0:~$
```




