# Overview : Lab 10 Installing and Deploying Software with PDQ
This repository documents my home lab experience focused on Installing and Deploying Software with PDQ using VirtualBox. The lab involves setting up PDQ Deploy and PDQ Inventory to automate software deployment and manage system configurations across multiple virtual machines.

## Objectives
- Learn PDQ Deploy: Explore how to automate the installation of software applications across multiple virtual machines.
- Understand PDQ Inventory: Set up and configure PDQ Inventory for system management and monitoring.
- Network Configuration: Use VirtualBox to simulate a network environment with different configurations and virtual machines.
## Documentation
In this home lab, I will demonstrate how to install PDQ Deploy, create software packages, and deploy them. We will be primarily using Windows Server 2022 for this lab environment. To begin, select Devices at the top of the VirtualBox menu, then choose Insert Guest Additions CD Image.
<br>
![image](https://github.com/user-attachments/assets/592c47ec-a41f-42d2-a91b-fee7673f9d74)

<br>

1. Now lets open up File Explore and we see that CD Drive (D) VirtualBox Guest additions has been added.

<br> 

![image](https://github.com/user-attachments/assets/e2049bd1-d68d-41af-98ee-c4bc701786ed)

<br> 

2.Double-click on VirtualBox Guest and click Next until you reach the Install option. Select Install, then choose Reboot now and click Finish. Once you log back into your Windows Server 2022 account, right-click on the gray folder icon in the system tray and select Shared Folders Settings....

<br>

![image](https://github.com/user-attachments/assets/9ed6201d-b8a2-4515-b809-2b1f58ed9c2d)

<br>

3. Next, click Add New Folder. Set the Folder Path to your Downloads folder, and create a new folder named "tobifash lab".

<br>

<img width="287" alt="Screenshot 2025-03-14 at 4 17 30 AM" src="https://github.com/user-attachments/assets/339f2764-f16a-40c3-8d42-ae4610b16c72" />

<br> 

4. After selecting the tobifash Lab folder, right-click on the disk icon at the bottom of the screen and select Remove Disk from Virtual Drive.

<br> 

![image](https://github.com/user-attachments/assets/28c40a12-270f-40b5-b328-64c7177e2102)

<br> 

5. Next we will go onto our web browser and go to [https://www.pdq.com/downloads/](https://www.pdq.com/downloads/ ) to download PDQ Deploy and PDQ Inventory.

<br> 

![Screenshot 2025-03-14 at 3 40 14 AM](https://github.com/user-attachments/assets/9562ec49-2b9d-48fc-a6e2-4651b0e2e217)


<br>

6. We can go back to our Windows Server 2022, open File Explorer, and see that the Z: drive for tobifash Lab is available. Once we open it, we will find the PDQ Deploy applications. We can then drag the application onto the desktop and begin the installation.

<br> 

![Screenshot 2025-03-14 at 4 21 40 AM](https://github.com/user-attachments/assets/28e0b1ee-a31c-4f12-af38-e675c60850f6)

<br> 

7. Once we open it, we will find the PDQ Deploy applications. We can then drag the application onto the desktop and begin the installation.
<br>

![Screenshot 2025-03-14 at 3 40 14 AM](https://github.com/user-attachments/assets/a759379f-395e-432d-b3a3-6bd025cad702)

<br> 

8. Select “Next” → accept the terms → “Next” then install.

<br> 

![image](https://github.com/user-attachments/assets/c19f42f1-7253-4273-a9e6-c8333a11dcbb)

<br>
9. Once the installation is finished, we can launch the application. Next we sign into our Administrator credentials.

<br> 

![Screenshot 2025-03-14 at 3 46 19 AM](https://github.com/user-attachments/assets/134d899d-73f3-4925-859f-e7a57b29a1d7)

10. Now that PDQ Deploy is ready, let's re-enable our internet connection. To do this, we need to go to Devices → Network → Network Settings, and change the setting to NAT. Then, open Control Panel → View Network Status and Tasks, and click on Change Adapter Settings. Right-click on Ethernet and select Properties. Next, double-click on Internet Protocol Version 4, and set it to Obtain an IP address automatically.

<br>

![image](https://github.com/user-attachments/assets/f0c88ac6-db04-46c3-a486-3a16a18b47c2)

<br> 

11. Our internet should now be active. To verify, we can open Command Prompt and ping google.com. 

![image](https://github.com/user-attachments/assets/cd7b28cf-3668-442a-9309-92a7ece20e2a)

<br> 

12. Additionally, the internet icon on the bottom right of the screen should be available, indicating a successful connection.

    <br>

    ![image](https://github.com/user-attachments/assets/99ea7e7a-e31a-4cd7-9e2f-d85c4376cb55)

<br>

13. Now, let's go back to PDQ Deploy and select "Extend" to activate the inactive subscription.

<br> 

![image](https://github.com/user-attachments/assets/055ce789-80b8-40db-ab90-fea0128a51da)

<br>

14. Extending the subscription will grant us a free trial of the Enterprise version, which allows access to all the available packages. We will need to enter our information and provide an email address. Once that's completed, we can start deploying packages using PDQ Deploy. Let's proceed by deploying Mozilla Firefox.

<br>

![image](https://github.com/user-attachments/assets/bd9d72d9-8b50-40dd-8648-62aa6c3800f0)

<br>

15. Double-click on the Mozilla Firefox package, and it will automatically start downloading. Once completed, it will appear in the Packages section.

<br> 

![Screenshot 2025-03-14 at 4 30 13 AM](https://github.com/user-attachments/assets/c3ea276a-5d7c-4202-82a9-049e15aedfe6)


<br> 

16. Right click on Mozilla Firefox and select “Deploy once”

<br> 

![Screenshot 2025-03-14 at 4 32 00 AM](https://github.com/user-attachments/assets/7e0325c8-9f1b-4fab-b8c4-5b2f3f3ef995)


<br> 

17. Then select “Choose targets” → “Active Directory” → “Computers”

<br> 

![Screenshot 2025-03-14 at 4 11 19 AM](https://github.com/user-attachments/assets/90dd8d11-cce3-430c-95fb-a55fcb8cebbf)

<br> 

18. Then select “Server2022” as our target then select “OK”.

<br>

![Screenshot 2025-03-14 at 4 11 41 AM](https://github.com/user-attachments/assets/bcc2251f-cc33-4dd7-ad62-9b023efb3caf)

<br> 

19. Select “Deploy Now”.

<br>

![Screenshot 2025-03-14 at 4 13 54 AM](https://github.com/user-attachments/assets/04588895-02cd-486d-a620-52e6faf2d089)

<br>

20. We have officially deploy Mozilla Firefox, the deploy worked perfectly and we can see that Firefox is installed onto our desktop.

<br> 

![Screenshot 2025-03-14 at 4 35 25 AM](https://github.com/user-attachments/assets/4dbbae40-b388-4bab-ac4c-16cceda56a76)

<br> 

21. Congratulations! We have successfully installed and set up PDQ Deploy, created and deployed software packages.

Now, let's switch back to a static IP. Open Control Panel and navigate to View Network Status and Tasks → Change Adapter Settings. Right-click on the network connection (Ethernet) and select Properties to begin configuring the network settings.

Enter the previously configured static IP settings:

- IP Address: 192.168.1.100
- Subnet Mask: 255.255.255.0
- Default Gateway: 192.168.1.1
- Preferred DNS Server:8.8.8.8
- Alternate DNS Server: 8.8.4.4

Click OK to apply the settings.

👉 [Next Lab 11 : PDQ Inventory: Hardware and Software Reporting](https://github.com/tobifash0/PDQ-Inventory-Hardware-and-Software-Reporting)
