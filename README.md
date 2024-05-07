# Splunk-Hands-On-Lab </br>

## Learning Objective </br>

In this lab, I will practice configuring, utilizing, and troubleshooting Splunk for cybersecurity operations, gaining hands-on experience in setting up data ingestion, conducting searches, generating reports, and responding to security incidents effectively.

## Setup </br>
Attack box and Target Machine were provided by TryHackMe

## Adding Data </br>
Uploading VPN logs to Splunk </br>
 </br>
<img src="https://cdn.discordapp.com/attachments/1237130346454057052/1237483822430421023/image.png?ex=663bd01e&is=663a7e9e&hm=3dc1739e0873b04f669b48a78b5884900bb791b44685e020538aea493553ae5e&"> </br>
 </br>
Review after inital configuration </br>
 </br>
<img src="https://cdn.discordapp.com/attachments/1237130346454057052/1237484724008652943/image.png?ex=663bd0f5&is=663a7f75&hm=8bb88d141f6247362f0aa4331237a12e3c1870f97889f3241d25a5436c44f2b0&"></br>

## Reconnaissance Phase </br>
In this search query we are going to look for the event logs in the index "botsv1" which contains the term imreallynotbatman.com </br>
 </br>
<img src="https://cdn.discordapp.com/attachments/1237130346454057052/1237492169942503464/image.png?ex=663bd7e4&is=663a8664&hm=39c8c40a07ccf7a605c95b800e8f2854995083d852f207752b8793efa37903b1&"> </br>
 </br>
In the sourcetype field, we saw that the following log sources contain the traces of this search type, "Suricata".  </br>
Suricata is an open-source based intrusion detection system and intrusion prevention system. </br>
We update our search query with the SRC and sourcetype  </br>
 </br>
<img src="https://cdn.discordapp.com/attachments/1237130346454057052/1237493049626726522/image.png?ex=663bd8b6&is=663a8736&hm=2c33797894b9a09f072d52c633665f23597b5c5d874837eedea8a744849f9135&"> </br>
 </br>
I narrowed my search on the source IP and examined the source type 'suricata' to identify triggered alerts. To find the the field containing signature alerts, I clicked on 'more fields' and added the signature alerts information field. </br>
 </br>
<img src="https://cdn.discordapp.com/attachments/1237130346454057052/1237493455131771002/image.png?ex=663bd917&is=663a8797&hm=a205019f4ee60441fcfb115a676885f1174ffcb3ead67f7d841c636719965733&"> </br>
 </br>

# Conclusion </br>
In this lab, we explored Splunk's role in cybersecurity, from setup to incident response. Through hands-on practice, we learned to configure Splunk, analyze data, and respond to security incidents effectively. From reconnaissance to resolution, Splunk proved invaluable, equipping us with the skills needed to navigate cybersecurity challenges with confidence.
