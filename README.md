# cka-lab-setup
This is steps to initialize kubernetes cluster
---
# prerequisites:
* 2 GB of free rams
* Vagrant installed
* VmWare Workstation installed

# Steps

* clone this repo into your machine
* go into directory
* install vagrant vmware plugin
```bash
vagrant plugin install vagrant-vmware-desktop
```
* start the machines
```bash
vagrant up
```
* ssh into control node
```bash
vagrant ssh control1
sudo apt update
sudo apt install jq -y
cd /cka
source setup-container.sh
source setup-kubetools.sh
```
* ssh also into worker1 and worker2 and apply these steps

* on control machine
```bash
sudo kubeadm init
```

* then add kubectl binary for this cluster and copy kubeadm join command into worker nodes you will find them after init process is completed.

* then add network CNI clalico or flannel.

* now cluster is ready you can check it with 
```bash
kubectl get nodes
```