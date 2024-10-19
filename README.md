<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This project involved setting up all the necessary prerequisites and installing osTicket from the ground up. This was carried out on a Windows 10 virtual machine that I created in Azure. osTicket is a popular and reliable open-source help desk ticketing system. 


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop Connection
- Internet Information Services (IIS)
- My SQL
<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Installation Steps</h2>
<p>
First thing to do when logging into Microsfot Azure is creating a Resource Group which you can find by typing in the search bar, give it any name you want then click review and create
</p>
<br />

<p>
After when the Resource Group is craeted, it's time to create the Virtual Machine
</p>
<br />














![image](https://github.com/user-attachments/assets/2421ecff-8f2c-48d5-af98-2ab4b1feac09)


<p>
Virtual Machine being set up 
</p>
<br />






![image](https://github.com/user-attachments/assets/70b0098c-4a68-48f1-a6a2-06fa84f1c973)










![image](https://github.com/user-attachments/assets/fb98a2f0-6309-4a7f-a862-1d629ce93f1d)




<p>
When setting up Virtual Machine leave all the other settings to default, once it's been created open remote Desktop Connection to connect to the VM (or Windows App for Mac which i'm using here) 
</p>
<br />



![image](https://github.com/user-attachments/assets/00369d75-f86f-4b9a-8fb5-6109acb61891)







![image](https://github.com/user-attachments/assets/984442dc-c01f-47d4-9b2f-b2f4a27ed8ec)








<p>
After connecting to the virtual machine, go install and enable IIS (Internet Information Services) by navigating to Control Panel > Programs > Turn Windows Features On or Off > Internet Information Services and enabling it. Then go to World Wide Web Services > Application Development Features and enable CGI. Next, open the Common HTTP Features dropdown and enable all the available features. After that, apply the changes.<br />









![image](https://github.com/user-attachments/assets/51257710-94b9-4a0c-a22b-f1905d057e48)



<p> I can verify the web server installation by entering the loopback IP (127.0.0.1) into the web browser, which should display the following page: <br />




![image](https://github.com/user-attachments/assets/88abae60-b4c9-460f-864b-f0c5d0ee2309)




<p> Next you need to download PHP Manager for IIS Setup: <br />



![image](https://github.com/user-attachments/assets/0c1e8c99-5096-4a9f-a436-931d497ffbfd)



<p> Install IIS URL Rewrite Module : <br />






![image](https://github.com/user-attachments/assets/67908069-c68e-4dea-b8a1-729f1f0d56ad)



<p>
After the installations are complete, create a PHP directory on the C drive.</p>
<br />



![image](https://github.com/user-attachments/assets/ecc2303a-6e36-4e80-99f4-e43456631860)






<p>
Now, download PHP and unzip the file into the PHP directory you created.</p>
<br />




![image](https://github.com/user-attachments/assets/311fc7f0-6d41-462e-85b5-8d8746614374)








<p>
Download Microsoft Visual C++:</p>
<br />




![image](https://github.com/user-attachments/assets/b82334b1-0f64-4f27-b907-27dd2399e237)





<p>
Download MySQL:</p>
<br />






![image](https://github.com/user-attachments/assets/7b9f61b0-f1a5-4bd7-8a30-463f013505ac)


<p>
Next, set up the login credentials and make a note of them to ensure you don't forget, as this is just for a project. In real-world scenarios, however, avoid writing down passwords.</p>
<br />





<p>
![image](https://github.com/user-attachments/assets/a3a6eb1b-6926-4198-bc3d-d9882d5d31c2)
</p>
<br />







<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />







<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />






<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />







<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />









<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />










<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />




































