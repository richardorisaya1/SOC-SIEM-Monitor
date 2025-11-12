# SOC/SIEM Monitoring (Creating a Honeypot)

<h2>Description</h2>
<br>The PowerShell script in this repository is responsible for parsing out Windows Event Log information for failed RDP attacks and using a third-party API to collect geographic information about the attacker's location. 
</br>

<br />
<br />
The script is used in this demo, where I set up Azure Sentinel (SIEM) and connect it to a live virtual machine acting as a honeypot.
We will observe live attacks (RDP Brute Force) from all around the world. I will use a custom PowerShell script to
Look up the attackers' Geolocation information and plot it on an Azure Sentinel Map!
<br />
<br />

<h2>Languages Used</h2>

- <b>PowerShell: Extract RDP failed logon logs from Windows Event Viewer</b>
- <b>KQL: Setup the logging of event information</b> 

<h2>Utilities Used</h2>

- <b>Azure Platform</b>
- <b>Microsoft Sentinel</b>
- <b>Event Manager</b>
- <b>Windows Defender Firewall with Advanced Security</b>
- <b>ipgeolocation.io:</b> IP Address to Geolocation API

<h2>Environments Used </h2>

- <b>Microsoft Azure virtual machine</b>

<h2>Program walk-through:</h2>

<p align="center">
<b>Turning the firewall off in all security settings to make the Virtual Machine enticing to the attacker:<br/> <br/>
<img src="https://imgur.com/rObIlP4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<b>Looking into the Event Manager to identify the failed login attempts:<br/>  <br/>
<img src="https://imgur.com/Hrp6523.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<b>Creating a script to parse WindowsEvents:<br/>  <br/>
<img src="https://imgur.com/3THFfmM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<b>Built customized log including geodata:<br/>  <br/>
<img src="https://imgur.com/uI5HhIP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<b>World map of incoming attacks after 24 hours:<br/>  <br/>
<img src="https://imgur.com/5ayACz3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
