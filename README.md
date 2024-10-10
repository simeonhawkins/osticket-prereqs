<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>


osTicket - Virtual Machine Setup

This tutorial covers the prerequisites, installation, and setup of the open-source help desk ticketing system, osTicket. osTicket provides a platform for creating and managing support tickets, allowing employees, users, or customers to submit and track their requests. We will guide you through the installation process, initial configuration, and utilization of osTicket’s core features. In this tutorial, we will deploy osTicket on Microsoft Azure, a cloud service that offers the infrastructure needed to create and host the virtual machines required for this lab.

Environments and Technologies Used

	•	Microsoft Azure (Virtual Machines/Compute)
	•	RDP (Remote Desktop Protocol)

Operating Systems Used

	•	Windows 10

Outline of Steps in Part One

In this part, we will:

	1.	Create a Resource Group.
	2.	Set up a Virtual Machine in the Azure resource group.
	3.	Connect to the VM using RDP.

Virtual Machine Setup

Step 1: Creating a Resource Group

<p align="center">
<img src="https://user-images.githubusercontent.com/128980344/228999887-c8db8e47-5c22-4b6e-bf59-6fdbc04e66cd.png" height="80%" width="80%" alt="Creating a Resource Group"/>
</p>


	•	Open the Azure Portal and either click on Resource Groups or search for it using the top search bar.
	•	Click Create at the bottom.
	•	Choose a region (e.g., US East). It’s recommended to keep all resources in the same region to avoid compatibility issues and unexpected costs.
	•	Name the resource group (e.g., osTicket-RG). Write down the name and region for reference.
	•	Click Review + Create, then Create once validated.

Step 2: Setting Up a Virtual Machine

<p align="center">
<img src="https://user-images.githubusercontent.com/128980344/229000988-75956759-edfc-4af7-aff3-d938866f8bb3.png" height="80%" width="80%" alt="Setting Up VM"/>
</p>


	•	Go back to the Azure homepage and click on Virtual Machines or search for it.
	•	Click Create and select Azure Virtual Machines.
	•	Fill in the following settings:
	•	Resource Group: Select the one created above.
	•	VM Name: (e.g., VM-1-osTicket-Lab).
	•	Image: Select Windows 10.
	•	Region: Match the region of your resource group.
	•	Availability Options: Select No infrastructure redundancy required.

<p align="center">
<img src="https://user-images.githubusercontent.com/128980344/229002483-0fc2e9ab-62c7-4514-bec3-60f02b2232d4.png" height="80%" width="80%" alt="VM Configuration"/>
</p>


	•	Scroll down and select the VM Size. Choose a size with at least 2 vCPUs to ensure performance.
	•	Enter a Username (e.g., oslabuser) and a Password (e.g., Password12321). Write these down for later use.
	•	Select the checkbox for licensing at the bottom.

<p align="center">
<img src="https://user-images.githubusercontent.com/128980344/229003230-b4a19e3e-d935-4272-8d3c-d0afbb04cb8c.png" height="80%" width="80%" alt="VM Username and Password"/>
</p>


Step 3: Configuring Networking and Finalizing the VM

	•	Click Networking on the top tab.
	•	Azure will automatically create a Virtual Network for you. Ensure the settings match your desired configuration.
	•	Click Review + Create and allow it to validate.
	•	Once validated, click Create. The deployment may take some time.

<p align="center">
<img src="https://user-images.githubusercontent.com/128980344/229168973-7bd8f8eb-f3aa-40dc-8971-538e445ff549.png" height="80%" width="80%" alt="VM Deployment"/>
</p>


Step 4: Connecting to the VM using RDP

	•	Once the deployment is complete, navigate back to Virtual Machines in the Azure portal.
	•	Select the VM (e.g., VM-1-osTicket-Lab).
	•	Copy the Public IP Address displayed on the right.

<p align="center">
<img src="https://user-images.githubusercontent.com/128980344/229169860-e059a965-30c5-4c34-a48e-1abdfe6d1f4b.png" height="60%" width="60%" alt="Public IP Address"/>
</p>


	•	On your Windows desktop, search for Remote Desktop Connection (RDP).
	•	Enter the Public IP Address of your VM and click Connect.

<p align="center">
<img src="https://user-images.githubusercontent.com/128980344/229403077-096a5d2d-8261-45b8-b837-2fbe38f25d44.png" height="50%" width="50%" alt="RDP Connection"/>
<img src="https://user-images.githubusercontent.com/128980344/229403360-e7233172-a419-46e3-8378-d66fb7bc2883.png" height="50%" width="50%" alt="RDP Login"/>
</p>


	•	Enter the Username and Password created earlier (e.g., oslabuser and Password12321).
	•	Click OK and accept the connection by clicking Yes.

Step 5: Completing the VM Setup

<p align="center">
<img src="https://user-images.githubusercontent.com/128980344/229172217-f634a6d5-2066-4b17-a564-90ace922c995.png" height="50%" width="50%" alt="Windows Setup"/>
</p>


	•	After connecting, choose your Privacy Settings. You can turn off all options for this lab.
	•	Once you reach the Windows desktop, the VM setup is complete.

You are now ready for the --> <a href="https://github.com/simeonhawkins/post-install-config"> NEXT STEP </a>
