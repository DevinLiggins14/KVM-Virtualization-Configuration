# KVM-Virtualization-Configuration
<h2>Description</h2>
The goal of this project is to configure Kernel-based Virtual Machine (KVM) virtualization on a CentOS server to create and manage virtualized environments. Define virtual machine settings, network configurations, and storage allocations to optimize performance and resource utilization.

<p align="center">
<img src="http://technewskb.com/wp-content/uploads/2017/01/linux-kvm.png"/>

<h2>Languages and Utilities Used</h2>

Bash 

<h2>Environments Used </h2>

- <b> 5.14.0-503.el9.x86_64 </b>

<h2>Project walk-through:</h2>
<p align="center">
  <br/> First install all KVM related packages on CentOS and start the libvirt service <br/>
<img src="https://github.com/user-attachments/assets/3078bf3a-e814-4f7b-b7cf-182414ab6df8"/>
  <br/> Explanation:
qemu-kvm: KVM package for QEMU, the hypervisor.
libvirt: Manages virtualization.
libvirt-daemon-*: Daemon configurations for network and KVM support.
virt-install: CLI tool for creating VMs.
virt-manager: GUI tool for managing VMs.
systemctl enable --now libvirtd: Enables and starts the libvirt service. <br/>
  <br/> Run lscpu to verify hardware support for virtualization <br/>
 <img src="https://github.com/user-attachments/assets/10dde927-f164-4728-be57-b313788552c8"/>
  <br/> Now create a storage pool for virtual machine disk images <br/>
  <img src="https://github.com/user-attachments/assets/6d614805-ed7e-496b-a5f7-982cfd30d212"/>
  <br/> mkdir -p /var/lib/libvirt/images: Creates a directory for storage.
virsh pool-define-as: Defines a storage pool with type dir.
virsh pool-start: Starts the storage pool.
virsh pool-autostart: Ensures the pool starts on boot. <br/>
  <br/> Now configure network settings for virtual machines  <br/> 
  <img src="https://github.com/user-attachments/assets/c52f2191-2ac9-4be5-9b27-2cbc891f3e01"/>
<br /> Now create a virtual machine using virtsh, virt manager, or virt-install <br/>
 <img src="https://github.com/user-attachments/assets/67c17b49-6dcb-40dd-83c4-96a47c2cd07a"/>
 <br /> 
 <br/> Now confirm the VM creation  <br/>
 <img src="https://github.com/user-attachments/assets/c93206b8-898a-494b-b2d7-0d234d97ae0e"/>
 <br /> run virsh edit centos9-vm to configure the VM that we have created   <br/>
 <img src="https://github.com/user-attachments/assets/34359bc0-dafd-466d-9227-be68adf14caa"/>
 <br /> 
 <br/> Add configurations  <br/>
 <img src="https://github.com/user-attachments/assets/546741b7-3f96-444a-b417-330baa531577"/>
  <br /> Attach newly created disk volume and configure disk image formats <br/>
 <img src="https://github.com/user-attachments/assets/278a4f3b-f9e4-4fc2-bf51-b6de0a5f7b55"/>
 <br /> 
 <br/>   <br/>
 <img src=""/>
  <br />  <br/>
 <img src=""/>
 <br /> 
 <br/>   <br/>
 <img src=""/><br />  <br/>
 <img src=""/>
 <br /> 
 <br/>   <br/>
 <img src=""/><br />  <br/>
 <img src=""/>
 <br /> 
 <br/>   <br/>
 <img src=""/><br />  <br/>
 <img src=""/>
 <br /> 
 <br/>   <br/>
 <img src=""/><br />  <br/>
 <img src=""/>
 <br /> 
 <br/>   <br/>
 <img src=""/><br />  <br/>
 <img src=""/>
 <br /> 
 <br/>   <br/>
 <img src=""/><br />  <br/>
 <img src=""/>
 <br /> 
 <br/>   <br/>
 <img src=""/><br />  <br/>
 <img src=""/>
 <br /> 
 <br/>   <br/>
 <img src=""/><br />  <br/>
 <img src=""/>
 <br /> 
 <br/>   <br/>
 <img src=""/><br />  <br/>
 <img src=""/>
 <br /> 
 <br/>   <br/>
 <img src=""/><br />  <br/>
 <img src=""/>
 <br /> 
 <br/>   <br/>
 <img src=""/><br />  <br/>
 <img src=""/>
 <br /> 
 <br/>   <br/>
 <img src=""/><br />  <br/>
 <img src=""/>
 <br /> 
 <br/>   <br/>
 <img src=""/><br />  <br/>
 <img src=""/>
 <br /> 
 <br/>   <br/>
 <img src=""/><br />  <br/>
 <img src=""/>
 <br /> 
 <br/>   <br/>
 <img src=""/><br />  <br/>
 <img src=""/>
 <br /> 
 <br/>   <br/>
 <img src=""/><br />  <br/>
 <img src=""/>
 <br /> 
 <br/>   <br/>
 <img src=""/>
