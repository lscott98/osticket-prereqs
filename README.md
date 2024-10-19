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



![image](https://github.com/user-attachments/assets/a40c56ed-f384-4770-8fac-7fbff626905d)









<p>
Open IIS as an admin:</p>
<br />


![image](https://github.com/user-attachments/assets/d2d75517-fa9d-46fa-863b-6e37f9689e38)






<p>
Next, navigate to PHP Manager, select "Register new PHP version," and then choose the specified file.</p>
<br />




![image](https://github.com/user-attachments/assets/d8e789d4-3cbe-4135-a187-de1589b7baff)





<p>
Return to the osticketVM Home, and under Manage Server on the right side, click Restart.</p>
<br />


![image](https://github.com/user-attachments/assets/3c68e99e-7287-4c48-9d2f-f15e8dec207e)




<p>
Next download osTicket and copy the upload file to the wwwroot file in the inetpub directory:</p>
<br />


![image](https://github.com/user-attachments/assets/7d8dc52c-7e5c-489e-93c8-34f2a21fb87d)






<p>
Reload IIS and restart the server as I did before, then click Browse *80 (http) on the right side:</p>
<br />


![image](https://github.com/user-attachments/assets/3510d21e-7dc7-4107-ad1f-7ba65ac83806)







<p>
This page should open: <br />

![image](https://github.com/user-attachments/assets/a2733e82-68f5-4a3e-9c76-fca7fe836383)





<p>
You'll notice that some extensions are not enabled. To enable them in IIS, go to Sites > Default Web Site > osTicket. Then, click on PHP Manager and select "Enable or disable an extension." Enable php_imap.dll, php_intl.dll, and php_opcache.dll.</p>
<br />


![image](https://github.com/user-attachments/assets/ce4ce800-ed8e-475a-9218-460f7f31d8de)





<p>
See the changes there 
<br />


![image](https://github.com/user-attachments/assets/6cf8914f-15bc-40b6-ac75-9bf2aa083d53)





<p>
Next, navigate to C drive > osTicket > include in File Explorer and rename ost-sampleconfig.php by removing "sample" from the filename.</p>
<br />

![image](https://github.com/user-attachments/assets/a8513c80-a3b2-437b-8f9a-766882a653e2)




<p>
Right-click on ost-config.php> Properties> Security> Advanced> Disable Inheritance> Remove all inherited permissions from this object:</p>
<br />



![image](https://github.com/user-attachments/assets/08bcd11f-40ec-4522-92eb-a13b26bdb53a)




<p>
Click the Add button to assign permissions to the file. Select a principal, type "Everyone," click Check Names, then click OK. Ensure all permissions are checked, then click OK again, followed by Apply and OK.</p>
<br />


![image](https://github.com/user-attachments/assets/5c067a5b-c813-4f40-9e76-b2828286d7f0)





<p>
Hit continue on the osTicket web page in the browser and fill out the set up page:<br />


![image](https://github.com/user-attachments/assets/509d8520-a1a2-4e32-bd2a-189cd47b1b50)






<p>
Before setting up the database, you'll need to connect to it using HeidiSQL. Install HeidiSQL using the setup links provided.</p>
<br />



![image](https://github.com/user-attachments/assets/2408153d-9734-4b49-9437-0231edbe1f5f)





<p>
In HeidiSQL click New> Username = root> Password = mySQL password from mySQL setup> Open:</p>
<br />



![image](https://github.com/user-attachments/assets/62ea6998-a8a3-4fac-b4b0-c7e7cec638d2)







<p>
In HeidiSQL, right-click on Unnamed, select Create, and then choose New Database. Name the database osTicket and click OK. After that, proceed to complete the database section of the osTicket setup. Click Install Now when you're finished.</p>
<br />



![image](https://github.com/user-attachments/assets/c3f6a6bf-0629-401a-aab7-507a4709fc76)





<p>
For the final steps, navigate to C drive > inetpub > wwwroot > osTicket, locate the setup file, and delete it. Then go to C drive > inetpub > wwwroot > osTicket > include, right-click on ost-config.php, select Properties, then go to Security, and click on Advanced. Select Everyone, click Edit, and ensure that only Read & Execute and Read are checked. Finally, apply the changes.</p>
<br />


![image](https://github.com/user-attachments/assets/cace3442-3e04-4a52-9597-ac4e25272f31)
























