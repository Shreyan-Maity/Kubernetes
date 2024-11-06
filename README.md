# Kubernetes
This repo holds all my Kubernetes learnings
# Here’s a guide for installing Kubernetes (specifically, Minikube, a popular tool for running Kubernetes locally) on Windows and Linux.


---

1. Installing Kubernetes (Minikube) on Windows

Prerequisites

1. Hardware: Minimum 2 CPUs, 2GB of free memory.


2. Software: Windows 10/11 or Windows Server 2019.


3. Tools:

Install Hyper-V (if not available, you can use Docker Desktop or VirtualBox as alternatives).

Install kubectl, the Kubernetes CLI tool.

Minikube: Download and install Minikube for local Kubernetes clusters.




Installation Steps

1. Install kubectl:

Download the installer from the kubectl release page.

Add kubectl to your system path.



2. Install Minikube:

Download the Minikube installer for Windows from the Minikube release page.

Run the installer and follow the prompts.



3. Start Minikube:

Open Command Prompt or PowerShell.

Run the following command to start a Kubernetes cluster:

minikube start --driver=hyperv

If you are using Docker or VirtualBox, replace --driver=hyperv with the relevant driver.



4. Verify Installation:

Run kubectl get nodes to verify that Minikube has created a Kubernetes cluster.





---

2. Installing Kubernetes (Minikube) on Linux

Prerequisites

1. Hardware: Minimum 2 CPUs, 2GB of free memory.


2. Software: Linux distribution (Ubuntu, CentOS, etc.), Virtualization enabled (check via grep -E --color 'vmx|svm' /proc/cpuinfo).


3. Tools:

Docker or a virtualization tool (such as VirtualBox).

kubectl.

Minikube.




Installation Steps

1. Install kubectl:

curl -LO "https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x kubectl
sudo mv kubectl /usr/local/bin/


2. Install Minikube:

curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube


3. Start Minikube:

Run the following command to start Minikube:

minikube start --driver=docker

If Docker is not available, you can specify a different driver, such as VirtualBox (--driver=virtualbox).



4. Verify Installation:

Run kubectl get nodes to check the Minikube Kubernetes cluster.





---

Additional Tips

Accessing Kubernetes Dashboard:

minikube dashboard

Stopping Minikube:

minikube stop

Deleting Minikube Cluster:

minikube delete


This setup will allow you to practice Kubernetes locally on both Windows and Linux.

