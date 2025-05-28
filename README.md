# Virtual-Machines-and-Remote-Desktops
Resource Group is created to hold Virtual Machines

Creating the first VM (virtual machine) specifically a windows virtual machine

Since I am creating two VMs and examing the traffic between those two I will create Virtual Network Within the Resource Group To hold the two Virtual Machines.

The Second Virtual Machine is a Linux VM then I attach it to the same Virtual Network that the windows one is in.

Next I examine the traffic between the two VMs
![Screenshot 2025-05-28 112133](https://github.com/user-attachments/assets/8fdb0f2d-f68a-4be1-9258-6a29f33eb96b)

To access the Remote Desktop I Use the IP address of the windows vm that was created and use remote desktop connection 
![Screenshot 2025-05-28 115603](https://github.com/user-attachments/assets/d74d3573-c99f-4bbf-bfd1-2991af2b01fb)

Once Inside the VM I download a program named wireshark this is needed to see the ICMP traffic going on between the two VMs

The ICMP traffic is used to test the connectivity between two devices

In the windows VM I open up Microsoft Power Shell then I command ping with the private IP address odf the linux VM
![Screenshot 2025-05-28 124401](https://github.com/user-attachments/assets/e4684d0f-f766-4586-8007-34a9f94c8562)

On wire shark I now see the network traffic going on from both the windows VM and the Linux VM 
![Screenshot 2025-05-28 124844](https://github.com/user-attachments/assets/2e752d72-9bc1-4247-a9e4-859d768e604d)

As you can tell the windows VM private IP address is 10.0.0.4 and the Linux is 10.0.0.5
