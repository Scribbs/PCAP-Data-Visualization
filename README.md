# 3D_Network_Graph

This repo contains all the materials needed to display the interconnections of IP addresses derived from Wireshark CSV PCAP exports. Here are the steps that I follow after downloading the report to a local directory.

1) Run a capture on any interface that you would like in Wireshark. Once you believe you have enough, stop the capture and then go to File -> Export Packet Dissections -> As CSV. Name the file whatever you would like and remember the location.
2) Start a Jupyter Notebook and upload the 


09/08/2020

Initial Files for 3D Force Directed Network Mapping with External API calls for Data Enirchment.

8 SEP 2020 - JMH
Users must have alienvault account
Users must add exception for site to allow multiple pop-up windows for api calls to service enrichments.

25 JUN 2021
Users must edit the network_3d.html file to apply your own api keys for Shodan and Virustotal.
  
  .onNodeClick(node => { window.open(`https://otx.alienvault.com/indicator/ip/${node.name}`, '_blank'),
                               window.open(`https://api.shodan.io/shodan/host/${node.name}?minify=True;key=(Your API Key Here`, '_blank'),
                               window.open(`https://www.virustotal.com/vtapi/v2/ip-address/report?apikey=(Your API Key Here)&ip=${node.name}`, '_blank')});
Links to API informaiton:

VirusTotal - https://support.virustotal.com/hc/en-us/articles/115002100149-API
Shodan - https://developer.shodan.io/
AlienVault - https://otx.alienvault.com/api


Acknowledgements:
 When I started out to craft this process I was able to find resources that were close to what I wanted to do but required minor tweaks to be able to work.
 
 The original JS for creating the force directed graph belongs to Vasco Asturiano and can be found in https://github.com/vasturiano/3d-force-graph
 The python used within the Jupyter notebook was discovered while digging through Austin Taylor's repos https://github.com/austin-taylor . I don't remember excalty which one, but he has a lot of cool stuff, so check him out.
