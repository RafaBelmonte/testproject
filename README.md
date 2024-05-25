![image](https://github.com/RafaBelmonte/testproject/assets/170759303/14d38ccf-5153-4849-9bd1-7aa4dced2ed8)

<h1>Creating Resource Groups and VMs (Azure)</h1>
This tutorial teaches you to create a Resource Group and a Virtual Machine in Azure and connect to it through Remote Connection.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Resource Groups)
- Remote Desktop

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)

<h2>Deployment and Configuration Steps</h2>

- Creating the Resource Group
- Creating and configuring the Virtual Machine inside the Resource Group
- Connecting to the VM using Remote Desktop Connection

<h2>Creation and Deployment Steps</h2>

![image](https://github.com/RafaBelmonte/testproject/assets/170759303/2d814b64-6875-4469-bbee-991977049595)


![image](https://github.com/RafaBelmonte/testproject/assets/170759303/a301fa40-53df-45c8-acc9-22a58a8ea1e1)

First, to create our Resource Group we can either utilize the search bar on Azure and search for "Resource Groups" as indicated on the first image, or you can use the direct link to the creation page as indicated on the second image.
</p>
<br />

![image](https://github.com/RafaBelmonte/testproject/assets/170759303/3e4f96a3-0952-4c5c-8564-e27099ec8b2c)


After reaching the Resource Groups creation page, you can choose between using the Create icon on the top left part of your screen, or hte ircon in the middle of your screen as indicated by the red arrows.
</p>
<br />

![image](https://github.com/RafaBelmonte/testproject/assets/170759303/572346f2-4190-4095-878b-7b272581a447)

Make sure to name your Resource Group and pick the appropriate Region depending on your personal location. After that, click on Review + create, and after it has been validated, click on create and wait for Azure to create your Resource Group.
</p>
<br />

![image](https://github.com/RafaBelmonte/testproject/assets/170759303/3d587ad8-a028-4c27-b1ec-865221e93bef)

When your Resource Group has been created, this is what you should see on your RG page.
</p>
<br />

![image](https://github.com/RafaBelmonte/testproject/assets/170759303/4578bbf5-548d-4c16-aca4-2df96c1a5c28)

This is what you will see when you click on your Resource Group. As you can see, we do not have any Resources in it yet. So in the next few images, we will be creating a virtual machine (VM) and accessing it using Windows Remote Desktop Connection
</p>
<br />

![image](https://github.com/RafaBelmonte/testproject/assets/170759303/7f71e8a5-abde-488a-a62e-6d50fbc64679)

Open your search bar and look for Virtual Machines. Click on it and let's start configuring our machine so we can deploy it inside our RG. The creation page for virtual machines is basically identical to the Resource Groups page, so you can refer to the 3rd image on this tutorial and click on Create. On the drop down menu pick "Azure Virtual Machine".
</p>
<br />

![image](https://github.com/RafaBelmonte/testproject/assets/170759303/716cbd28-fec8-4097-aa6e-a2b25477dfeb)

This is what our VM creation page should look like. I used a red arrow to highlight some important steps. First, use the Resource Group drop down menu to select your RG so you can create your machine inside the group. The second arrow was added because on the Free Version of Azure, some machine sizes are not available on certain Availability Zones, so depending on your needs you might need to switch availability zones to make sure you can create the machine with the size that you need. In this case I'm utilizing Zone 2 to create a 2vcpus, 16GiB memory machine.
Before creating the machine you will have to create a username and password, those will be used to connect to your virtual machine so it is imperative that you remember these or you wont have access to it once created.
Lastly, Review and Create. After passing the validation, click on "Create" at the bottom left of your screen and wait for Azure to create and deploy your vm. (Note: Depending on your zone, size of machine and time of day, deployment can take a few minutes)
</p>
<br />

![image](https://github.com/RafaBelmonte/testproject/assets/170759303/db8702af-f731-47f0-8ea3-922cba7a2da4)

![image](https://github.com/RafaBelmonte/testproject/assets/170759303/0fdf4c25-a334-4423-b9bc-6dfce3edb920)


Once your machine has been successfully created and deployed, you should see this page and click on "Go to resource" where all the information on your virtual machine is displayed, including its Public IP address (which we will use to connect to our VM) and other information that are not relevant for this specific tutorial.
</p>
<br />

![image](https://github.com/RafaBelmonte/testproject/assets/170759303/551bedb0-df13-45ba-b426-93d9c932b875)

Use your Windows search bar to search for Remote Desktop Connection. Open it and input your VMs public IP into the program. After that, click on Show Options as indicated by the red arrow.
</p>
<br />

![image](https://github.com/RafaBelmonte/testproject/assets/170759303/9e1e6fb0-325c-44df-8ad9-463c8d59c99a)

Input the username you picked while creating your machine and click connect. It will request the password you created with your username
</p>
<br />

![image](https://github.com/RafaBelmonte/testproject/assets/170759303/de3f8c74-c24e-46d8-bb5b-e49c8cd22896)

This is what you should see if your username and password were input correctly. Click on "Yes" and your virtual machine should load.
</p>
<br />

![image](https://github.com/RafaBelmonte/testproject/assets/170759303/0f66ff9b-a350-471b-899b-52635188eff0)

No need to select any of these, since this is just a tutorial and we wont actually be doing anything inside the VM at this point.
Click Accept and your VM is now running!
You did it! Good job!

![image](https://github.com/RafaBelmonte/testproject/assets/170759303/0ba58d4d-b1df-40fd-9d32-f7e1513c29c6)

![image](https://github.com/RafaBelmonte/testproject/assets/170759303/77c72a23-9c9a-4256-b0da-4410e05671ee)

![image](https://github.com/RafaBelmonte/testproject/assets/170759303/4d808a3e-5899-44c7-bb64-f63aa693c83d)



PS: After testing creating your resource group and virtual machine DO NOT FORGET to delete them after you are done as Azure will keep them connected and it will start draining your credits!!! You can do that by navigating to https://portal.azure.com/ selecting each one of your created resources and clicking on DELETE (Azure will create a second Resource Group named NetworkWatcherRG which also needs to be deleted). Wait for it to finish and when it is done, double check it!
</p>
<br />
