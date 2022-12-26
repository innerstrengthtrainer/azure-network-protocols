<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Full Video Demonstration</h2>

- ### [Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.flexclip.com/share/18365971e2ede90187a9dff8c5e5bcba1fbb9e4.html)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Create two VMs, one as windows 10 and one as Ubuntu Server
- Open Windows 10 VM and install Wireshark
- Using Wireshark and command line, explore network protocols

<h2> Abbreviated Actions and Observations</h2>

<p>
<img src="https://user-images.githubusercontent.com/47663923/209569486-c3e15f60-edd8-4867-8cec-d0ca77d5508b.png" height="80%" width="80%" alt="Pinging Virtaul Machine"/>
</p>
<p>
To initiate our review of ICMP traffic, I first continuously ping VM2 using the private IP address using command ping 10.0.0.5 -t. This allows us to see what changes when we change networking rules.
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/47663923/209569724-6d58e5d6-590a-4bbf-bfd9-678e0fc46528.png" height="80%" width="80%" alt="SSH log in"/>
</p>

<p>
Log into VM2 using SSH on VM1 in command line.
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/47663923/209570009-3397dfab-4735-4eaf-b36a-7d6f215a80e0.png" height="80%" width="80%" alt="DHCP"/>
</p>
<p>
Using DHCP to renew our IP address and observing on Wireshark.
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/47663923/209570164-defb8af1-3a44-4bc3-a0ba-b9109815eb54.png" height="80%" width="80%" alt="DHCP"/>
</p>
<p>
Using RDP (tcp.port == 3389) in Wireshark to observe the traffic.
</p>
<br />
