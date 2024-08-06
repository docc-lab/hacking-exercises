# Instructions for playing with Kubernetes in CloudLab using HotelReservation

This tutorial familiarizes participants with basic Kubernetes Operations, such as setting resource allocations for containers and scaling up/down a pod.  

## Start Initialize the cluster 

1. Choose the deathstarbench-k8s-setup profile, which is part of the Tracing-Pythia project.
2. Enter the profile configuration options
     1. DeathStarBench in this profile is pre-built to work with Intel Machines, so choose machines w/Intel CPUs.  Good choices include c6525-25g and c6525-100g in CloudLab Utah.  
     2. You may or may not wish to increase the number of nodes.
     3. You can leave the rest of the options as default.
3.  You will receive two emails, one indicating the clsuter is setting up and another indicating the cluster is ready.  Wait for the latter email before trying to use the cluster.  It can take up to 15 min. 

4.  Read the README for deathstarbench-k8s-setup profile, which provides detailed information about the profile and how deathstarbench is configured.

## Start Hotel Reservation
1. Follow the instructions in deathstarbench-k8s-setup profile to start HotelReservation.

## Explore Kubernetes Commands
