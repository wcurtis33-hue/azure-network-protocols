125
<br />-Install Wireshark to begin analyzing network traffic.<br />
</p>
<br />

<p>
<img src="https://i.imgur.com/DfuUTYy.png" height="80%" width="80%" alt="Azure Networking Steps"/>
</p>
<p>
<br />-Apply a filter for ICMP traffic in Wireshark.<br />
<br />-Open PowerShell and run the ping command to test network communication.<br />
<br />-Test communication with the Ubuntu VM using its private IP and with google.com.<br />
<br />-Initiate a continuous ping to the Ubuntu VM using: ping -t (IP address) to observe network security groups.<br />
</p>
<br />

<p>
<img src="https://i.imgur.com/16ERkju.png" height="80%" width="80%" alt="Azure Networking Steps"/>
</p>
<p>
<br />-Access the networking settings for the Ubuntu VM in the Azure portal.<br />
<br />-Create an inbound security rule to block ICMP traffic.<br />
<br />-Set the rule's priority higher than SSH (300) to ensure it takes precedence.<br /> 
</p>
<br />

<p>
<img src="https://i.imgur.com/uIQktM5.png" height="80%" width="80%" alt="Azure Networking Steps"/>
</p>
<p>
<br />-Open the Azure portal and configure networking settings for the Ubuntu VM.<br />
<br />-Add an inbound security rule to block ICMP traffic, setting priority above SSH (300).<br />
<br />-Check the Windows VM and confirm ICMP traffic is blocked.<br />
<br />-Modify the rule to allow ICMP traffic.<br />
<br />-Run the continuous ping to ensure it resolves without timeouts.<br />
</p>
<br />

<p>
<img src="https://i.imgur.com/Tt5Tswg.png" height="80%" width="80%" alt="Azure Networking Steps"/>
</p>
<p>
<br />-Examine SSH traffic by logging into the Ubuntu server via PowerShell using the ssh command.<br />
<br />-Filter SSH traffic in Wireshark with tcp.port == 22.<br />
<br />-View session activity in Wireshark, where each command executed on the Ubuntu server is logged.<br />
</p>
<br />

<p>

</p>
<br />

<p>
<img src="https://i.imgur.com/fCf8jry.png" height="80%" width="80%" alt="Azure Networking Steps"/>
</p>
<p>
<br />-Filter DNS traffic in Wireshark using udp.port == 53.<br />
<br />-Use the nslookup command to query google.com and disney.com.<br />
<br />-Observe the results of the DNS lookup for these popular sites.<br /> 
</p>
<br />

<p>
<img src="https://i.imgur.com/Xr7AGGZ.png" height="80%" width="80%" alt="Azure Networking Steps"/>
</p>
<p>
<br />-Filter RDP traffic in Wireshark using tcp.port == 3389.<br />
<br />-Observe continuous traffic as RDP streams live data between the computer and the VM hosted on Azure.<br />
</p>
<br />

<h2>Lessons Learned </h2>

The goal of the lab was to observe how different protocols and ports are used in network communication between devices.
Although the lab didn’t focus on troubleshooting, it provided valuable information.
I learned that troubleshooting requires tools like Wireshark and the command line to understand how traffic flows through network ports and protocols.
I realized that success in troubleshooting depends on both familiarity with the tools and maintaining an inquisitive mindset.
