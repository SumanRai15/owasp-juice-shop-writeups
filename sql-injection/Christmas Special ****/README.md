<h1>Owasp-Juice-Shop WriteUps</h1>
<h2>Christmas Special ****</h2>
<h3>Main goal of this lab is to purchase <b>Christmas Super-Surprise-Box</b> </h3>
<h3>We need to find vulnerable parameter within the webpage to search for <b>Christmas Super-Surprise-Box</b> which is hidden. </h3>
<br></br>

<p>This lab demonstrates how we can exploit a server using <b>Search</b> option.</p>
<p>In the below image we can see the home page of Owasp-Juice-Shop that we will be going to exploit. On the top right we can see <b>Search</b> option.</p>

 <div align="center">
<a href="images/01.png">
 <img src="images/01.png" width="1600"/>
</a>
  
**Figure 1:** HomePage.

</div>

<p><b>Step 1:</b> We use the search option and use BurpSuite to capture the traffic to know how the <b>search</b> function is working behind the scene.</p>

<p>We can use <b>'--</b> paylod in the search parameter (?q) to check whether the given webpage is vulnerable to <b>SQLi</b>. Since we got 500 Internal server error now we can confirm that the search parameter is vunerable. </p>

 <div align="center">
<a href="images/02.png">
 <img src="images/02.png" width="1600"/>
</a>
  
**Figure 1:** Inspecting Search function using BurpSuite.

</div>

<p><b>Step 2:</b>Since we can't find Christmas product directly , we need to use SQLi payload in search parameter to list out all hidden products. For this we use <b>'))--</b> payload.</p>
<div align="center">
<a href="images/03.png">
 <img src="images/03.png" width="1600"/>
</a>
  
**Figure 1:** Inspecting Search function using BurpSuite.

</div>
