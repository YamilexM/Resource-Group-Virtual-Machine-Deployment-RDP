# Azure Resource Group, Virtual Machine Deployment & RDP

## Objective

Review and manage an Azure Windows virtual machine, verify its supporting resources, confirm RDP access, and validate the remote system.

## Step 1: Review the Resource Group

Reviewed the Azure resource group and identified the resources supporting the virtual machine.

![](images/01-resource-group-resources.png)

## Step 2: Verify the VM Deployment

Confirmed that the virtual machine deployment completed successfully.

![](images/02-vm-deployment-succeeded.png)

## Step 3: Review the Virtual Machine

Reviewed the VM configuration, including the operating system, region, size, and networking information.

![](images/03-virtual-machine-overview.png)

## Step 4: Start the Virtual Machine

Started the VM and confirmed that its status changed to **Running**.

![](images/04-vm-running.png)

## Step 5: Verify RDP Access

Confirmed that **port 3389** was accessible for Remote Desktop connectivity.

![](images/05-rdp-access-verified.png)

## Step 6: Connect to the Windows VM

Successfully connected to the Windows virtual machine using Remote Desktop.

![](images/06-rdp-connected-to-windows-vm.png)

## Step 7: Verify the Remote System

Used `hostname` and `ipconfig` to verify the VM identity and private IP address from inside the remote session.

![](images/07-vm-hostname-and-private-ip.png)

## Skills Demonstrated

- Microsoft Azure
- Azure Virtual Machines
- Resource Group Management
- Virtual Networking
- Remote Desktop Protocol (RDP)
- Windows Administration
- Deployment Verification
- Cloud Infrastructure
