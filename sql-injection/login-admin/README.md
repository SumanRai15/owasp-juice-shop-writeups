#Owasp-Juice-Shop WriteUps
 The main goal of this is to log in as Administrator's user account.

 Here we have the login page. At first I tried to check if the given login page is vulnerable to SQL Injection or not. To check I added single colon in the email field and a random password.
 <div align="center">

### Figure 1: Login Page

<img src="images/01.png" width="600"/>

**Figure 1:** Initial login page.

</div>
 After intercepting the request in Burpsuite, we can now confirm that the given login page is vulnerable to SQl Injection since we got "500 Internal server error" in the response.

 <div align="center">



<img src="images/02.png" width="600"/>

**Figure 1:** Inspecting Login request with Burpsuite.

</div>

In the next step I tried to exploit with basic SQLi payload i.e. ' OR 1=1 with random password value.

<div align="center">

### Figure 1: Login Page

<img src="images/01-login-page.png" width="600"/>

**Figure 1:** Initial login page.

</div>

 

