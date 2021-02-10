# WVD Firewall Policy Sample
author: Nathan Swift

This WVD Firewall policy can be deployed and used with Azure Firewall Premium to protect your WVD Host Pools, Rule sets are based on [Azure Docs Here](https://docs.microsoft.com/en-us/azure/firewall/protect-windows-virtual-desktop) and also based on testing.

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fswiftsolves-msft%2FAzureFirewall%2Fmaster%2FFirewallPolicySamples%2FWVDFirewallPolicy%2Fazuredeploy.json" target="_blank">
    <img src="https://aka.ms/deploytoazurebutton"/>
</a>
<a href="https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fswiftsolves-msft%2FAzureFirewall%2Fmaster%2FFirewallPolicySamples%2FWVDFirewallPolicy%2Fazuredeploy.json" target="_blank">
<img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.png"/>
</a>


Use the following format for the Array data for WVDServiceBusURLs, WVDBlobURLs, WVDTableURLs, WVDQueueURLs

```["gsmUNIQUESTRINGeh.servicebus.windows.net/*","gsmUNIQUESTRINGeh.servicebus.windows.net/*"]```

![New app](https://github.com/swiftsolves-msft/AzureFirewall/blob/master/FirewallPolicySamples/WVDFirewallPolicy/images/urls.png?raw=true)

Use the following format for the Array data for AD_DNSServers

```["xx.xx.xx.xx","yy.yy.yy.yy"]```

![New app](https://github.com/swiftsolves-msft/AzureFirewall/blob/master/FirewallPolicySamples/WVDFirewallPolicy/images/addcspic.png?raw=true)
