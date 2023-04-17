<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1> Various Network Protocols and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH,DNS, DHCP, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Have your azure subcription
- Make your resource group
- Azure Windows VM1 and Linux VM2 

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/GWtWQ4Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Starting from azure hub im going to open up my windows vm1, while in vm1 im going to install wireshark so from my vm browser im going to type wireshark and install 
once done ill will run wireshark and what wireshark does is shows all the live traffic thats happening on the vm1.The first protocol im going to practice with is
ICMP which stand for internet control message which ping uses to test network connectivity.so when im  within vm1 if i were to ping  vm2 ip address using CMD we would then see a ping and reply from vm2 to vm1 in the wireshark hub.


</p>
<br />

<p>
<img src="https://i.imgur.com/0C8s9Yh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In my next protocol im going to practice with is SSH which is secure shell which is the same as RDP but without any extra stuff just command line.                 Again from wireshark im going to filter for ssh traffic only so from powershell ise im going to use use ssh instead of ping to access to vm2 using 
the username created for both vm  so sshe labuser@ vm2 ip address.
</p>
<br />

<p>
<img src="https://i.imgur.com/Hv7jQq0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
My next protocol ill use is DHCP which stand for dynamic host configuration,what it does is automatically assigns your IP address.what im going to be doing is
force dhcp to renew a new ip address for vm1, by using ipconfig /renew.
</p>
<br />


<p>
<img src="https://i.imgur.com/2xqA1oH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next protocol ill practice with is domain name system or DNS.with dns it turn human language into language computers can understand and read. if i wanted to look up google ill go into  powershell again. ill type nslookup www.google.com, i would then get google ip address.

