## Requirement (Linux) 
* Virtualization must be enabled in the BIOS setting ([Virtualization ON](https://docs-old.fedoraproject.org/en-US/Fedora/13/html/Virtualization_Guide/sect-Virtualization-Troubleshooting-Enabling_Intel_VT_and_AMD_V_virtualization_hardware_extensions_in_BIOS.html)). 
* VirtualBox Or KVM


> Note: I am trying the Installation process is with KVM . And Kubernet need virtualization so turn on the function before trying the process.

## KVM installation 
* use `sudo apt-get install qemu-kvm libvirt-bin bridge-utils virt-manager` to install KVM and support library.
* We also need to add our user to the `libvrtd` group using `sudo adduser name libvirtd` ,because KVM virtual Machice access is only for root and the libvrtd group members. 

> Note: Sometime linvrtd group is missing then you have create it yourself  `sudo addgroup libvirtd`


## Simple Task in KVM
* To get the VM list : `virsh -c qemu:///system list`
* To Start VM manager : search for `virtual machine` in ubuntu app search



## To Use Kubernet localy install minikube
`sudo curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 && chmod +x minikube && sudo mv minikube /usr/local/bin/`



Source :   
[KVM installation](https://www.howtogeek.com/117635/how-to-install-kvm-and-create-virtual-machines-on-ubuntu/)
