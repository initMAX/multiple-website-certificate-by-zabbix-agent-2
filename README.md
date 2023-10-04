
# Multiple Website certificate by Zabbix agent 2

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
|{$CERT.ARRAY}|Array of elements - hostname:port:IP where each element in the array is delimited by a comma.|`<hostname1>:<443>:<IP1>,<hostname2>:<443>:<IP2>`|
|{$CERT.EXPIRY.WARN}|Number of days until the certificate expires.|`7`|
|{$CERT.WEBSITE.HOSTNAME}|The website DNS name for the connection.|`<Put DNS name>`|
|{$CERT.WEBSITE.IP}|The website IP address for the connection.|`` |
|{$CERT.WEBSITE.PORT}|The TLS/SSL port number of the website.|`443`|