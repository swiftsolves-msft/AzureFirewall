## Allow Additional Windows Virtual Desktop

Further information on Azure Firewall and WVD can be found here: https://docs.microsoft.com/en-us/azure/firewall/protect-windows-virtual-desktop

*NOTE: To provide granular tight allowance please do the following, Thank you Erick Moore for the guidance.

1.	Register your virtual machines to the Windows Virtual Desktop host pool.

2.	Open Event viewer, then go to Windows logs > Application > WVD-Agent and look for Event ID 3701.

3.	Whitelist the URLs that you find under Event ID 3701. The URLs under Event ID 3701 are region-specific. You'll need to repeat the unblocking process with the relevant URLs for each region you want to deploy your virtual machines in.

Within the sample rule update XX.XX.XX.XX/YY << Is your WVD Host Pool Subnet

Within the sample rule update ZZ.ZZ.ZZ.ZZ << Is your AD DNS Server IP

For Network FQDN ensure you are using either DNSProxy at https://docs.microsoft.com/en-us/azure/firewall-manager/dns-settings

or within the ARM Firewall Deployment DNSSettings as

```"dnsSettings": {
"servers": [],
"enableProxy": false,
"requireProxyForNetworkRules": false
},
```