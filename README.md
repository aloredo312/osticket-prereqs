<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Installation Steps</h2>

<p>
<img width="781" alt="install:enable iss" src="https://github.com/user-attachments/assets/5a10cc5d-973f-4537-b5ea-0f18965cf88e">
</p>
<p>
To Install and enable IIS in Windows along with CGI, we go to the control panel. From there we go to programs and features, we check the Internet Information Services box. Then to install CGI we expand Internet Information Services and go under World Wide Web Services, then go under Application Development Features and right there we can check the box for CGI to turn it on. We hit ok and wait for it to install.
</p>
<br />

<p>
<img width="344" alt="install php manager" src="https://github.com/user-attachments/assets/c542e830-2dfb-410e-a85c-2aa6468852d1">
</p>
<p>
To install PHP manager we go to the osTicket files, find and select the PHP file (PHPManagerForIIS_V1.5.0.msi) and follow the set up steps to install it.
</p>
<br />

<p>
<img width="342" alt="install rewrite module" src="https://github.com/user-attachments/assets/eed248af-d855-4c43-a9c9-31a5f94d6eaf">
</p>
<p>
To install the Rewrite Module we go to the same osTicket files, find and select the Rewrite Module file (rewrite_amd64_en-US.msi) and follow the steps to install it.
</p>
<br />

<p>
<img width="461" alt="create directory for php" src="https://github.com/user-attachments/assets/e598f12a-89e3-4b0f-8b9c-de3086adb6a6">
</p>
<p>
To create a directory for PHP we can open a file explorer and go to the C drive. There we create a new folder and call it PHP all caps. 
</p>
<br />

<p>
<img width="829" alt="extract php file folders" src="https://github.com/user-attachments/assets/0dfc03db-3fdf-430f-837c-12a656e32325">
</p>
<p>
Then we can go back to the osTicket files folder and unzip the PHP 7.3.8 file and extract it into the "C:PHP" folder that we created in the previous step. To do this we right click the PHP file in the osTicket files forlder and select extract all. Then we click browse and select the "C" drive, then select "PHP", click "select folder", and then we can click extract.
</p>
<br />

<p>
<img width="333" alt="install vc redistributable file" src="https://github.com/user-attachments/assets/00574096-95a3-4cc3-ad76-72a70a16032b">
</p>
<p>
To install VC Redistributable we go to the osTicket files forlder and select the VC_redist.x86.exe file. From there just follow the steps on the set up window.
</p>
<br />

<p>
<img width="341" alt="install mysql database" src="https://github.com/user-attachments/assets/7ae96de2-4556-4da8-845b-25dcaca41328">
</p>
<p>
To install the mysql database select the file on the osTicket files folder (mysql-5.5.62.msi). In the set up window select "typical set up" and install.
</p>
<br />

<p>
<img width="346" alt="configure mysql" src="https://github.com/user-attachments/assets/839eab74-c729-460b-a0b9-d7d12bccc872">
</p>
<p>
Once finished installing we Launch Configuration Wizard and select "standard configuration". We will set up a password in this example I used "root" only to keep it simple. Finish the rest of the set up by selecting "next" and "finish".
</p>
<br />

<p>
<img width="643" alt="register php within iss" src="https://github.com/user-attachments/assets/859f09ea-e414-4b57-a9bb-3a73df2af232">
</p>
<p>
We're going to open IIS as an admin by going to the start and searching  up "Internet Information Services", then we will right click and select "run as administrator". Once opened select "PHP manager" and select "register new php version". Then we browse, select the C drvie, select "PHP" folder and double click on "php-cgi" and click "ok". Then we reload IIS by selecting "stop" and then "start" on the right side under "manage server".
</p>
<br />

<p>
<img width="464" alt="install osTicket" src="https://github.com/user-attachments/assets/1531d93d-a060-4698-98b2-13d6923445b8">
</p>
<p>
From the osTicket installation files folder we extract the osTicket-v1.15.8zip and copy the "upload" folder into "C:inetpub\wwwroot". Within the "c:\inetpub\wwwroot" we rename "upload" to "osTicket". We need to reload IIS, so we open IIS and stop then start the server. Note that some extensions are not enabled. If you want to enable extensions you can go back to IIS, select sites, then default, then osTicket and double click on PHP Manager. Here you can click "enable" or "disable" an extension. For exmaple I enabled: "php_imap.dll", "php_intl.dll", and "php_opcache.dll". Then you have to refresh the osTicket site in your browser and you will see the changes.
</p>
<br />

<p>
<img width="476" alt="install heidisql   create session" src="https://github.com/user-attachments/assets/83ee6135-cd8d-42f5-bc00-3e9b47725097">
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="641" alt="create a osticket database" src="https://github.com/user-attachments/assets/bc3a53a0-678f-4f93-adb2-d22dfb6af2aa">
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="635" alt="finish installing osticket" src="https://github.com/user-attachments/assets/99ec76bc-2dd6-4805-b692-8ef533827f72">
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
