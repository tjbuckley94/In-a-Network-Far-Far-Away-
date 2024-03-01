# In-a-Network-Far-Far-Away-
<h3>Mission 1</h3>  

Issue: With the DoS attack, the Empire took down the Resistance's DNS and primary email servers.  

The Resistance's network team was able to build and deploy a new DNS server and mail server.  

The new primary mail server is asltx.1.google.com, and the secondary should be asltx.2.google.com.  

The Resistance (starwars.com) is able to send emails but unable to receive any.  

Your Mission:  

Determine and document the mail servers for starwars.com using nslookup.  

Explain why the Resistance isn't receiving any emails.  

Document your suggested DNS corrections.  

1. Mail servers for starwars.com

 &emsp;&emsp;**Server:		2001:558:feed::1  
 &emsp;&emsp;Address:	2001:558:feed::1#53**  

 &emsp;&emsp;**Non-authoritative answer:  
 &emsp;&emsp;starwars.com	mail exchanger = 5 alt2.aspmx.l.google.com.  
 &emsp;&emsp;starwars.com	mail exchanger = 1 aspmx.l.google.com.  
 &emsp;&emsp;starwars.com	mail exchanger = 10 aspmx2.googlemail.com.  
 &emsp;&emsp;starwars.com	mail exchanger = 5 alt1.aspx.l.google.com.  
 &emsp;&emsp;starwars.com	mail exchanger = 10 aspmx3.googlemail.com.**  

 &emsp;&emsp;**Authoritative answers can be found from:  
&emsp;&emsp;aspmx3.googlemail.com	internet address = 64.233.171.27  
&emsp;&emsp;aspmx3.googlemail.com	has AAAA address 2607:f8b0:4003:c15::1b  
&emsp;&emsp;alt2.aspmx.l.google.com	internet address = 64.233.171.27  
&emsp;&emsp;alt2.aspmx.l.google.com	has AAAA address 2607:f8b0:4003:c15::1b  
&emsp;&emsp;aspmx.l.google.com	internet address = 173.194.203.27  
&emsp;&emsp;aspmx.l.google.com	has AAAA address 2607:f8b0:400e:c03::1a  
&emsp;&emsp;aspmx2.googlemail.com	internet address = 142.250.115.26  
&emsp;&emsp;aspmx2.googlemail.com	has AAAA address 2607:f8b0:4023:1004::1b**  

2. Explain why the Resistance isn't receiving any emails

&emsp;&emsp;**The resistance isn’t receiving any emails because the URLs for the email servers are not correct**

3. Suggested DNS corrections

&emsp;&emsp;**Asltx.1.google.com  
&emsp;&emsp;asltx.2.google.com**  


<h3>Mission 2</h3>
Issue: Now that you've addressed the mail servers, all emails are coming through. However, users are still reporting that they haven't received mail from the theforce.net alert bulletins.  

Many of the alert bulletins are being blocked or going into spam folders.  

This is probably due to the fact that theforce.net changed the IP address of their mail server to 45.23.176.21 while your network was down.   

These alerts are critical for identifying pending attacks from the Empire.  

Your Mission:  

Determine and document the SPF for theforce.net using nslookup.  

Explain why the Force's emails are going to spam.  

Document your suggested DNS corrections.  


1. Sender Policy Framework (SPF) of theforce.net:  

&emsp;&emsp;**Server:		2001:558:feed::1
&emsp;&emsp;Address:	2001:558:feed::1#53**

&emsp;&emsp;**Non-authoritative answer:  
&emsp;&emsp;theforce.net	text = "google-site-verification=XTU_We07Cux-6WCSOItl0c_WS29hzo92jPE341ckbOQ"  
&emsp;&emsp;theforce.net	text = "v=spf1 a mx a:mail.wise-advice.com mx:smtp.secureserver.net include:aspmx.googlemail.com ip4:45.63.15.159 ip4:45.63.4.215  ~all"  
&emsp;&emsp;theforce.net	text = "google-site-verification=ycgY7mtk2oUZMagcffhFL_Qaf8Lc9tMRkZZSuig0d6w"**  

<h3>Mission 3</h3>
Issue: You have successfully resolved all email issues and the Resistance can now receive alert bulletins. However, the Resistance is unable to easily read the details of alert bulletins online.  

They are supposed to be automatically redirected from their subpage resistance.theforce.net to theforce.net.  
Your Mission:  

Document how a CNAME should look by viewing the CNAME of www.theforce.net using nslookup.  

Explain why the subpage resistance.theforce.net isn't redirecting to theforce.net.  

Document your suggested DNS corrections.  

1. Document the CNAME records:

&emsp;&emsp;**Server:		2001:558:feed::1  
&emsp;&emsp;Address:	2001:558:feed::1#53**  

&emsp;&emsp;**Non-authoritative answer:  
&emsp;&emsp;www.theforce.net	canonical name = theforce.net.**  

2. Explain why the subpage resistance.theforce.net isn't redirecting to theforce.net  

&emsp;&emsp;**The subpage isn’t redirecting because the canonical name listed is theforce.net**  

3. Suggested DNS corrections

&emsp;&emsp;**The correct canonical name should be resistance.theforce.net instead of theforce.net**  

<h3>Mission 4</h3>
Issue: During the attack, it was determined that the Empire also took down the primary DNS server of princessleia.site.  

Fortunately, the DNS server for princessleia.site is backed up and functioning.  

However, the Resistance was unable to access this important site during the attacks, and now they need you to prevent this from happening again.  

The Resistance's networking team provided you with a backup DNS server of: ns2.galaxybackup.com.  

Your Mission:  

Confirm the DNS records for princessleia.site.  

Document how you would fix the DNS record to prevent this issue from occurring again.  

1. Confirm the DNS records for princessleia.site

&emsp;&emsp;**Server:		2001:558:feed::1  
&emsp;&emsp;Address:	2001:558:feed::1#53**  

&emsp;&emsp;**Non-authoritative answer:  
&emsp;&emsp;princessleia.site	nameserver = ns26.domaincontrol.com.  
&emsp;&emsp;princessleia.site	nameserver = ns25.domaincontrol.com.**  

&emsp;&emsp;**Authoritative answers can be found from:  
&emsp;&emsp;ns25.domaincontrol.com	internet address = 97.74.102.13  
&emsp;&emsp;ns25.domaincontrol.com	has AAAA address 2603:5:2161::d  
&emsp;&emsp;ns26.domaincontrol.com	internet address = 173.201.70.13  
&emsp;&emsp;ns26.domaincontrol.com	has AAAA address 2603:5:2261::d**  

<h3>Mission 5</h3>
Issue: The network traffic from the planet of Batuu to the planet of Jedha is very slow.  

You have been provided a network map with a list of connected planets between Batuu and Jedha.  

It has been determined that the slowness is due to the Empire attacking Planet N.  

Your Mission:  

View the Galaxy Network MapLinks to an external site., and determine the OSPF shortest path from Batuu to Jedha.  
<img width="864" alt="Galaxy_Network_map" src="https://github.com/tjbuckley94/In-a-Network-Far-Far-Away-/assets/124013280/13526476-b670-4bfd-9560-cf96a769cd87">

Confirm that your path doesn't include Planet N in its route.  

Document the shortest path so that the Resistance can use it to develop a static route to improve the traffic.  

1. Document the shortest OSPF path from Batuu to Jedha

&emsp;&emsp;**OSPF path  
&emsp;&emsp;batuu-D-C-E-F-J-I-L-Q-T-V-jedha  
&emsp;&emsp;OSPF path cost  
&emsp;&emsp;23**  

<h3>Mission 6</h3>  
Issue: The Resistance is determined to seek revenge for the damage the Empire has caused with all of its attacks.  

You are tasked with gathering secret information from the Dark Side network servers that can be used to launch network attacks against the Empire.  

You have captured some of the Dark Side's encrypted wireless internet traffic in the following PCAP: Dark Side PCAPLinks to an external site..  

Your Mission:  

Figure out the Dark Side's secret wireless key by using Aircrack-ng.  

1. Wireless key

&emsp;&emsp;**dictionary**  

2. Host IP addresses and MAC addresses  

&emsp;&emsp;**Sender MAC address  
&emsp;&emsp;Cisco-Li_e3:34:01 (00:0f:66:e3:34:01)  
&emsp;&emsp;Sender IP address  
&emsp;&emsp;172.16.0.1  
&emsp;&emsp;Target MAC address  
&emsp;&emsp;IntelCor_55:98:ef (00:13:ce:55:98:ef)  
&emsp;&emsp;Target IP address  
&emsp;&emsp;172.16.0.101**  

<h3>Mission 7</h3>
Issue: As a thank you for saving the Galaxy, the Resistance wants to send you a secret message!  

Your Mission:  

View the DNS record from Mission 4. The Resistance provided you with a hidden message in the TXT record. Follow the steps included in the message.  

&emsp;&emsp;**Ran nslookup -type=txt princessleia.site**  

&emsp;&emsp;**Server:		2001:558:feed::1  
&emsp;&emsp;Address:	2001:558:feed::1#53**  

&emsp;&emsp;**Non-authoritative answer:  
&emsp;&emsp;princessleia.site	text = "Run the following in a command line: telnet towel.blinkenlights.nl or as a backup access in a browser: www.asciimation.co.nz"**  


![StarWars1](https://github.com/tjbuckley94/In-a-Network-Far-Far-Away-/assets/124013280/af06c1cc-dd5f-4fb4-b546-2b63fc337f48)  
![StarWars2](https://github.com/tjbuckley94/In-a-Network-Far-Far-Away-/assets/124013280/646ed5d4-1b1a-4587-93d1-6958b6bd2acf)  

