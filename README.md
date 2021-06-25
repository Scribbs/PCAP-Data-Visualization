# 3D_Network_Graph


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
