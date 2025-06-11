# Virtual-Machines-and-Remote-Desktops
A Resource Group is created to hold Virtual Machines.

I will be creating two Virtual Machines, creating the first VM (virtual machine) specifically a Windows virtual machine.

![Screenshot 2025-06-10 175525](https://github.com/user-attachments/assets/3fea9d55-8fe8-4615-beaf-3d4f700d76a4)

In the image above the most important settings to apply to make sure it is the windows VM we need is in the image option and selecting Windows 10 Pro and not another image like linux.

Since I am creating two VMs and examining the traffic between those two, I will create a Virtual Network within the Resource Group to hold the two Virtual Machines.

while creating the Windows VM on the network settings section there is an option where it will create a default virtual network instead seleact create new and change the name to Lab2-vnet, like the image below.

![Screenshot 2025-06-10 182026](https://github.com/user-attachments/assets/41a68be6-0fad-4526-b9ee-5b7a196306dd)


The Second Virtual Machine is a Linux VM, to make the VM into a Linux VM make sure the image has this ubuntu server applied, like in the image below.

![Screenshot 2025-06-11 062057](https://github.com/user-attachments/assets/0e1dafe1-8542-4107-92f0-395857f004ae)

It will automatically be put in the lab 2 vnet virtual network when creating the new VM.

Next, I examine the traffic between the two VMs
![Screenshot 2025-05-28 112133](https://github.com/user-attachments/assets/8fdb0f2d-f68a-4be1-9258-6a29f33eb96b)

To access the Remote Desktop, I use the IP address of the Windows VM that was created, and use Remote Desktop Connection 
![Screenshot 2025-05-28 115603](https://github.com/user-attachments/assets/d74d3573-c99f-4bbf-bfd1-2991af2b01fb)

Once inside the VM, I download a program named Wireshark. This is needed to see the ICMP traffic going on between the two VMs

The ICMP traffic is used to test the connectivity between two devices

In the Windows VM, I open up Microsoft Power Shell, then I command ping with the private IP address of the Linux VM
![Screenshot 2025-05-28 124401](https://github.com/user-attachments/assets/e4684d0f-f766-4586-8007-34a9f94c8562)

On Wireshark, I now see the network traffic going on from both the Windows VM and the Linux VM 
![Screenshot 2025-05-28 124844](https://github.com/user-attachments/assets/2e752d72-9bc1-4247-a9e4-859d768e604d)

As you can tell, the Windows VM private IP address is 10.0.0.4, and the Linux VM is 10.0.0.5
