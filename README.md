<h1>Penetration Test and Report</h1>


<h2>Description</h2>
The project was an assessment to provide an analysis of security flaws present in MegaCorpOne’s web applications, networks, and systems. This assessment was conducted to identify exploitable vulnerabilities and provide actionable recommendations on how to remediate the vulnerabilities to provide a greater level of security for the environment.
<br />


<h2>Tools and Techniques Used</h2>

- <b>Cross-Site Scripting</b>
- <b>OSINT</b>
- <b>LFI and directory traversal</b>
- <b>Nmap</b>
- <b>Nessus</b>
- <b>Metasploit</b>
- <b>Remote Code Execution</b>
- <b>Privilege escalation</b>
- <b>Enumeration</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)
- <b>Kali-Linux - virtualbox</b>

<h2>Program walk-through:</h2>

<p align="center">
Cross-site scripting: 
 Entered a java script that created the pop-up “Help!”
<script>alert(“HELP”)</script>
 <br/>
<img src="https://i.imgur.com/SrlgRoF.png" height="80%" width="80%" alt="P2.Flag3"/>
<br />
<br />
Local file inclusion: 
 Uploaded a php script on the VR Planner page that allowed access to the back-end of the web application <br/>
<img src="https://imgur.com/2cQ4HRc.png" height="80%" width="80%" alt="P2Flag5 LFI"/>
<img src="https://imgur.com/A9ci8Ps.png" height="80%" width="80%" alt="P2.Flag9"/>
<br />
<br />
Unprotected username and password: 
 A search of the public web application page source revealed a username (dougquaid) and password (kuato) for the Admin Login <br/>
<img src="https://imgur.com/1EHnkdI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/5KH3xqw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Nmap Scan: 
 A Nmap scan 192.168.13.0/24 provided a list of available hosts with open ports. We were able to view the ports/protocols, service type, and versions. This information gives an attacker the ability to search for common vulnerabilities to use to exploit the hosts. 
  Syntax: Nmap -sV 192.168.13.0/24 <br/>
<img src="https://imgur.com/nIS0x04.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Vulnerability scan/ Remote code execution:
  Nessus and Metasploit:  A Nessus scan revealed that there is a critical vulnerability to the Apache Struts version on the remote host. We were able to execute the exploit via Metasploit. This exploit established a reverse shell, which allowed access to the host to explore files. <br/>
<img src="https://imgur.com/k6OxDcq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://imgur.com/J8cB2Pw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://imgur.com/v26Yz0e.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Remote code execution:  
 An aggressive Nmap scan revealed that there is a critical vulnerability to the Apache Tomcat version on the remote host. We were able to execute the exploit via Metasploit. This exploit established a reverse shell, which allowed access to the host to explore files. 
  Syntax: Nmap -A 192.168.13.10 <br/>
<img src="https://imgur.com/BVDrcNo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://imgur.com/9xfkgQn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://imgur.com/yj7e8dq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://imgur.com/JGszFyd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://imgur.com/5X6TUzb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</br>
<br />
Vulnerability scan/ Remote code execution:
  Nessus and Metasploit:  A Nessus scan revealed that there is a critical vulnerability to the Apache Struts version on the remote host. We were able to execute the exploit via Metasploit. This exploit established a reverse shell, which allowed access to the host to explore files. <br/>
<img src="https://imgur.com/ESphz02.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://imgur.com/EYIqmPn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://imgur.com/HBrekuU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Vulnerability scan/ Remote code execution:
  Nessus and Metasploit:  A Nessus scan revealed that there is a critical vulnerability to the Apache Struts version on the remote host. We were able to execute the exploit via Metasploit. This exploit established a reverse shell, which allowed access to the host to explore files. <br/>
<img src="https://imgur.com/ESphz02.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://imgur.com/EYIqmPn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://imgur.com/HBrekuU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Vulnerability scan/ Remote code execution:
  Nessus and Metasploit:  A nessus scan revealed that there is a critical vulnerability to the Apache Struts version on the remote host. We were able to execute the exploit via Metasploit. This exploit established a reverse shell, which allowed access to the host to explore files. <br/>
<img src="https://imgur.com/ESphz02.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://imgur.com/EYIqmPn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://imgur.com/HBrekuU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Vulnerability scan/ Remote code execution:
  Nessus and Metasploit:  A nessus scan revealed that there is a critical vulnerability to the Apache Struts version on the remote host. We were able to execute the exploit via Metasploit. This exploit established a reverse shell, which allowed access to the host to explore files. <br/>
<img src="https://imgur.com/ESphz02.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://imgur.com/EYIqmPn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://imgur.com/HBrekuU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
