# Multiple Website certificate by Zabbix agent 2

> **⚠️ This repository is DEPRECATED.**  
> Development has moved to an all‑new template that lives here:  
> 👉 <https://git.initmax.cz/initMAX-Public/zabbix-templates/-/tree/production/free/Multiple_Website_certificate_by_Zabbix_agent_2>  
> or
> 👉 <https://github.com/initMAX/Zabbix-Templates/tree/production/free/Multiple_Website_certificate_by_Zabbix_agent_2>  
>
> ### Why migrate?
> * **Monitor multiple certificates** – monitor several TLS/SSL certificates on a single host with a flexible array format
> * **Item Discovery Mode** – automatically creates items for each certificate target
> * **Host Discovery Mode** – optionally creates a dedicated virtual host for each monitored certificate
> * **Custom warning and critical thresholds** – easily define expiration alerts using macros
> * **Support for multiple ports and IPs** – flexible hostname:port:IP format for each check
> * **Native integration** – uses only Zabbix Agent 2, no external scripts or dependencies
> * **Fully compatible** with Zabbix 7.0 and higher
>
> Please open all new issues and pull‑requests in the new repository.

## Description

This template allows you to monitor multiple TLS/SSL certificates on a single host by Zabbix agent 2 without any external scripts.

## Requirements
 - Zabbix 6.0 or higher

## Setup

1\. Download the template and import it to Zabbix.

2\. Create a host for the TLS/SSL certificates with Zabbix agent interface.

3\. Link the template to the host.

4\. Customize the value of {$CERT.WEBSITE.HOSTNAME} macro.

5\. Customize the value of {$CERT.ARRAY} macro.

## Zabbix configuration

No specific Zabbix configuration is required.

### Macros used

|Name|Description|Default|
|----|-----------|-------|
|{$CERT.ARRAY}|Array of elements - hostname(:port(:IP)) where each host is delimited by a comma. The default port is '443'.|`<hostname1>(:<port1>(:<IP1>)),<hostname2>(:<port2>(:<IP2>)), ...`|
|{$CERT.EXPIRY.WARN}|Number of days until the certificate expires.|`7`|
|{$CERT.WEBSITE.HOSTNAME}|The website DNS name for the connection.|`<Put DNS name>`|
|{$CERT.WEBSITE.IP}|The website IP address for the connection.|`` |
|{$CERT.WEBSITE.PORT}|The TLS/SSL port number of the website.|`443`|

---
**Like, share and follow us** 😍 for more content:
- [LinkedIn](https://www.linkedin.com/company/initmax/)🔥
- [Twitter](https://twitter.com/initmax)
- [Instagram](https://www.instagram.com/initmax/)
- [Facebook](https://www.facebook.com/initmax)
- [Web](https://www.initmax.cz/)
- [Youtube](https://www.youtube.com/@initmax1)
