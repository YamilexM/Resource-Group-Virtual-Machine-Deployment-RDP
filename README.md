# Azure Resource Group, Virtual Machine Deployment & RDP

## Project Overview

In this lab, I worked with Microsoft Azure to review a deployed Windows virtual machine, verify the supporting Azure resources, confirm the deployment status, start the VM, validate Remote Desktop Protocol (RDP) access, and successfully connect to the Windows environment.

The goal was to gain hands-on experience with Azure virtual machines, resource groups, networking components, deployment verification, and remote administration.

## Technologies Used

- Microsoft Azure
- Azure Virtual Machines
- Azure Resource Groups
- Azure Virtual Network
- Network Security Groups
- Remote Desktop Protocol (RDP)
- Windows 11
- Windows Command Prompt

## What I Practiced

- Reviewing Azure resource group resources
- Identifying the components associated with a virtual machine
- Verifying a successful Azure deployment
- Reviewing virtual machine configuration
- Starting and managing a Windows VM
- Validating RDP connectivity
- Connecting remotely to a Windows VM
- Reviewing the VM's hostname and IP configuration
- Verifying the identity of the remote system
- Documenting a cloud infrastructure lab

## Step 1: Review the Resource Group

I opened the **RG-Labenv** resource group and reviewed the Azure resources associated with the virtual machine.

The resource group contained several components required to support the VM, including:

- Virtual machine
- Public IP address resource
- Network security group
- Virtual network
- Network interface
- Operating system disk

This helped me understand that an Azure virtual machine depends on multiple connected resources rather than operating as one standalone object.

![Resource Group Resources](images/01-resource-group-resources.png)

## Step 2: Verify the Virtual Machine Deployment

I opened the **Deployments** section of the resource group to confirm that the Windows virtual machine deployment completed successfully.

The deployment showed a **Succeeded** status along with the deployment completion time and duration.

This confirmed that the Azure resources were successfully provisioned.

![VM Deployment Succeeded](images/02-vm-deployment-succeeded.png)

## Step 3: Review the Virtual Machine Configuration

I opened the **VM1** overview page to review the virtual machine configuration.

The VM showed information including:

- **Virtual Machine:** VM1
- **Operating System:** Windows 11 Pro
- **Region:** East US 2
- **VM Size:** Standard D2ads v6
- **Virtual Network/Subnet:** VM1-vnet/default
- Attached networking resources

Reviewing the VM overview helped me become more familiar with where important compute and networking information is located within Azure.

![Virtual Machine Overview](images/03-virtual-machine-overview.png)

## Step 4: Start the Virtual Machine

The virtual machine had previously been stopped and deallocated, so I started the VM before attempting a remote connection.

After starting it, the VM status changed to:

**Running**

This confirmed that the virtual machine was powered on and ready for remote access.

![VM Running](images/04-vm-running.png)

## Step 5: Verify RDP Access

I opened the **Connect** section of the virtual machine and selected **Native RDP**.

Before attempting the connection, I used Azure's access check to verify that Remote Desktop traffic could reach the VM.

Azure confirmed:

**Port 3389 is accessible from source IP(s)**

This verified that the network configuration allowed the RDP connection to reach the virtual machine.

![RDP Access Verified](images/05-rdp-access-verified.png)

## Step 6: Connect to the Windows VM Using RDP

I downloaded the RDP connection file and opened it with a Remote Desktop client on my local computer.

After authenticating with the VM credentials, I successfully connected to the remote Windows environment.

The Windows 11 desktop loaded successfully, confirming that the Remote Desktop connection was working.

![RDP Connected to Windows VM](images/06-rdp-connected-to-windows-vm.png)

## Step 7: Verify the Remote System

After connecting to the virtual machine, I opened Command Prompt and ran:

```cmd
hostname
ipconfig
```

The `hostname` command returned:

```text
VM1
```

The `ipconfig` command showed the VM's private IPv4 address:

```text
10.0.0.4
```

This allowed me to verify from inside the remote session that I was connected to the expected Azure virtual machine and review its internal network configuration.

![VM Hostname and Private IP](images/07-vm-hostname-and-private-ip.png)

## Skills Practiced

- Microsoft Azure
- Azure Virtual Machines
- Resource Group Management
- Cloud Infrastructure
- Virtual Networking
- Network Security Groups
- RDP Configuration
- Remote Administration
- Windows Administration
- IP Configuration
- Command Prompt
- Deployment Verification
- Technical Documentation

## What I Learned

This lab helped me better understand how Azure virtual machines are built and managed.

I learned that a virtual machine relies on multiple Azure resources, including networking components, security rules, storage, and IP configuration.

I also practiced verifying a successful deployment, starting a virtual machine, confirming RDP access through port 3389, connecting remotely to a Windows environment, and using command-line tools to verify the hostname and private IP address from inside the VM.

This project gave me more hands-on experience with cloud infrastructure, remote administration, networking, and basic Azure troubleshooting.
