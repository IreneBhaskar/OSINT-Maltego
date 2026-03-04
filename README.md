<h1>OSINT: Maltego & Movie Piracy Sites</h1>

<h2>Purpose of Project</h2>
<p>This project aims to investigate how much information can be extracted from a URL. More specifically, if Maltego can identify locations or individuals behind pirated video streaming websites.</p>

<h2>Utilities Used</h2>
<p>
Linux VM - for a safe and resource conserving sandbox to experiment on.
   
Maltego - an OSINT tools that collects and neatly displays the relationship of information from public sources, such as: 
<ul>
   <li>social media accounts (reveal names, profile pictures, locations, social connections),</li>
   <li>WHOIS information (show owner, registrar, creation date, etc…),</li>
   <li>DNS records & SSL certificates (help to map servers and domains belonging to the same organisation),</li>
   <li>etc…</li>
</ul>
</p>

<h2>Project Walk-Through</h2>

<p align="center">
Step 1: Running Maltego on a Linux VM<br/>
<img src="image" height="80%" width="80%" alt="image description"/>
<br />
<br />
Step 2:  <br/>
<img src="image" height="80%" width="80%" alt="image description"/>
<br />
<br />
</p>

<h2>Findings</h2>
<p>
No matter which transforms were being run, it all points to Cloudflare.
   
Cloudflare is a **reverse proxy**, meaning that it sits between the user and the real server. This not only hides the real server from the user (**IP masking**) but also has the added benefits of filtering malicious traffic (e.g. prevents DDoS attacks) and improves the performance of the website through **caching**, which speeds up the delivery of data, and by spreading traffic across multiple servers (**load balancing**). 

This is particularly effective for a video streaming website since it:
<ul>
   <li>Improves the functionality of the website (footage plays smoothly) while also</li>
   <li>obscuring the physical server’s location. This protects the website owners from legal action hence allowing the sites to remain active longer.</li>
</ul>

This project’s investigation with Maltego ends here since attempts to bypass Cloudflare infringe on illegal activity.
</p>

<h2>Conclusion</h2>
<p>
It is not possible to legally identify individuals or locations of long standing movie piracy sites due to Cloudflare, a double edged sword that protects the website from being taken down while improving the video streaming quality at the same time.
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
