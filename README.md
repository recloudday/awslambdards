<h1>Using Secrets Manager to Authenticate with an RDS Database Using Lambda</h1>

<h2>Description</h2>
In this lab, I demonstrated how to use Secrets Manager to authenticate with an RDS database using Lambda. 
I began by creating a Lambda function, followed by creating and adding a custom layer for MySQL support. 
After editing the 'index.mjs' file to include the necessary code for database connectivity, I attached a policy to the Lambda function to grant access to Secrets Manager. 
I then created a secret in Secrets Manager to securely store the database credentials. 
As part of the lab, I updated the Lambda function to retrieve the credentials from Secrets Manager, ensuring secure authentication. After changing the database password, I updated the 'index.mjs' file in the RDS to reflect the new password. 
This lab highlighted my ability to securely manage database credentials using AWS Secrets Manager and Lambda, ensuring enhanced security and seamless integration.
<br />


<h2>Concepts and Utilities Used</h2>

- <b>AWS - Lambda</b>
- <b>RDS</b>
- <b>Secrets</b>
- <b>Security</b>

<h2>Environments Used </h2>

- <b>AWS</b>

<h2>Environment walk-through:</h2>

<p align="center">
Create Lambda Function: <br/>
<img src="https://imgur.com/e84XfsU.png" height="80%" width="80%" alt="Lambda Steps"/>
<br />
<br />
Create Layer and set runrume to 6s:  <br/>
<img src="https://imgur.com/vk1kIQ5.png" height="80%" width="80%" alt="Lambda Steps"/>
<br />
<br />
Add a custom layer:  <br/>
<img src="https://imgur.com/CDdijyT.png" height="80%" width="80%" alt="Lambda Steps"/>
<br />
<br />
Edit the index.mjs file on the RDS function:  <br/>
<img src="https://imgur.com/5KjCumZ.png" height="80%" width="80%" alt="Lambda Steps"/>
<br />
<br />
Test:  <br/>
<img src="https://imgur.com/CKv4pW4.png" height="80%" width="80%" alt="Lambda Steps"/>
<br />
<br />
Lambda -> Configuration -> Permissions -> role name -> Add permission:  <br/>
<img src="https://imgur.com/b0NVyY9.png" height="80%" width="80%" alt="Lambda Steps"/>
<br />
<br />
Create Secret:  <br/>
<img src="https://imgur.com/Qa4wzII.png" height="80%" width="80%" alt="Lambda Steps"/>
<br />
<br />
Password before:  <br/>
<img src="https://imgur.com/5QUTmDs.png" height="80%" width="80%" alt="Lambda Steps"/>
<br />
<br />
Lambda now has a Secrets Manager function:  <br/>
<img src="https://imgur.com/ZFaddLf.png" height="80%" width="80%" alt="Lambda Steps"/>
<br />
<br />
The password has now changed:  <br/>
<img src="https://imgur.com/imLDGzt.png" height="80%" width="80%" alt="Lambda Steps"/>
<br />
<br />
Replace the code in the function to use the update password function:  <br/>
<img src="https://imgur.com/Va6cfq1.png" height="80%" width="80%" alt="Lambda Steps"/>
<br />
<br />
Test again:  <br/>
<img src="https://imgur.com/lODMWsd.png" height="80%" width="80%" alt="Lambda Steps"/>
<br />
<br />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
