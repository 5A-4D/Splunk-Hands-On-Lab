# Splunk-Hands-On-Lab </br>

## Learning Objective </br>

In this lab, I will practice configuring, utilizing, and troubleshooting Splunk for cybersecurity operations, gaining hands-on experience in setting up data ingestion, conducting searches, generating reports, and responding to security incidents effectively.

## Setup </br>
Attack box and Target Machine were provided by TryHackMe

## Adding Data </br>
Uploading VPN logs to Splunk </br>
 </br>
<img src="https://i.imgur.com/e5mJl74.png"> </br>
 </br>
Review after inital configuration </br>
 </br>
<img src="https://i.imgur.com/BRsESHy.png"></br>

## Reconnaissance Phase </br>
In this search query we are going to look for the event logs in the index "botsv1" which contains the term imreallynotbatman.com </br>
 </br>
<img src="https://i.imgur.com/N0chhVH.png"> </br>
 </br>
In the sourcetype field, we saw that the following log sources contain the traces of this search type, "Suricata".  </br>
Suricata is an open-source based intrusion detection system and intrusion prevention system. </br>
We update our search query with the SRC and sourcetype  </br>
 </br>
<img src="https://i.imgur.com/gAPUSzL.png"> </br>
 </br>
I narrowed my search on the source IP and examined the source type 'suricata' to identify triggered alerts. To find the the field containing signature alerts, I clicked on 'more fields' and added the signature alerts information field. </br>
 </br>
<img src="https://i.imgur.com/wNU7Ogz.png"> </br>
 </br>

# Conclusion </br>
In this lab, we explored Splunk's role in cybersecurity, from setup to incident response. Through hands-on practice, we learned to configure Splunk, analyze data, and respond to security incidents effectively. From reconnaissance to resolution, Splunk proved invaluable, equipping us with the skills needed to navigate cybersecurity challenges with confidence.
