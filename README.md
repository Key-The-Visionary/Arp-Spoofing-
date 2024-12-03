# ARP Spoofing Attack

## Objective

- Conduct an ARP spoofing attack and understand how it is done step by step.
- Understand how to detect an ARP spoofing attack and write a Python script that
automates the process.
- Get hands-on practice with the Linux CLI.

### Skills Learned

- MITM Attack or On-the-path attack
- Write and test a Python script that automates the ARP spoofing attack.
- Learn to write Python programs that leverage the Scapy library to automate
cybersecurity tasks.


### Tools Used

- dsniff tool
- Scapy Library python script

## Steps

This screenshot shows the downloading and install of the dsniff tool that was used to carryout this arp spoofing attack. 

![arp spoofing screenshot 1](https://github.com/user-attachments/assets/85d36331-1696-43cd-80ae-576a5af3ffa1)

---------------------------------------------------------------------------------------------------------------


 This Next step was to use the netdiscover command to discover other ip addresses of other machines on the network and enable IP forwarding.

![arp spoofing screenshot 2](https://github.com/user-attachments/assets/e4342b11-40d5-47fd-950d-12b597cd321f)

--------------------------------------------------------------------------------------------------------------

Next, I ran the  sudo arpspoof -i eth0 -t 192.168.100.101 192.168.100.1 command to generate multiple fake ARP replies. I ran this command again in a new terminal with the ip addresses reversed to trick the router into believing I am the victim ip and then ran the urlsnarf tool to extract the urls of websites visited.

![arp spoofing screenshot 3](https://github.com/user-attachments/assets/fee8a30d-ae93-4718-a656-18a6f082b000)
![arp spoofing screenshot 4](https://github.com/user-attachments/assets/90118d6f-32fc-4579-a00d-a5bb9f720ee4)

--------------------------------------------------------------------------------------------------------------

In this step I generated some traffic on the metasploitable victim machine using the wget command/tool.  wget http://www.google.com


![arp spoofing screenshot 5](https://github.com/user-attachments/assets/29a09ff0-6659-4c39-905e-482e7670c970)
