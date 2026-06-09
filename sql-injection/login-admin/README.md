#Owasp-Juice-Shop WriteUps
 The main goal of this is to log in as Administrator's user account.

 Here we have the login page. At first I tried to check if the given login page is vulnerable to SQL Injection or not. To check I added single colon in the email field and a random password.
 <div align="center">

<img src="images/01.png" width="600"/>

**Figure 1:** Initial login page.

</div>
 After intercepting the request in Burpsuite, we can now confirm that the given login page is vulnerable to SQl Injection since we got "500 Internal server error" in the response.

 <div align="center">

<img src="images/02.png" width="1000"/>

**Figure 2:** Inspecting Login page.

</div>

In the next step I tried to exploit with basic SQLi payload in email field i.e. ' OR 1=1 & random password value.

<div align="center">

<img src="images/03.png" width="600"/>

**Figure 1:** Basic SQLi payload in email field.

</div>

We can inspect the request with the help of BurpSuite.

<div align="center">

<img src="images/04.png" width="1000"/>

**Figure 1:** Inspecting Response using BurpSuite.

</div>

This was still not working , so i though of commenting out everything after the email field by using double dash sign. Our paylod would look like <b>' OR 1=1--</b> & random password value.

<div align="center">

<img src="images/05.png" width="1000"/>

**Figure 1:** Updating Payload.

</div>
and as we can see this time it actually worked since we already figured out this lab was vulnerable to SQLi


<div align="center">

<img src="images/06.png" width="1000"/>

**Figure 1:** We have access to Administrator account.

</div>


 

