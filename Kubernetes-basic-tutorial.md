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

`kubectl` is the command for interfacing with and managing kubernetes clusters.  This [website](https://spacelift.io/blog/kubernetes-cheat-sheet) provide a nice overview of this commnd.  


