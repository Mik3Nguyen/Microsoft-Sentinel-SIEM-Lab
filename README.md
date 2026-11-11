# Microsoft-Sentinel-SIEM-Lab
## Project Overview
Cloud-based SIEM home lab using Sentinel, Microsoft Azure, KQL, and GeoIP threat visualization. This cybersecurity home lab focuses on configuring and deploying a cloud-based Security Information and Event Management (SIEM) environment that uses Microsoft Sentinel and Microsoft Azure. The objective of this lab was to gain hands-on experience with security event monitoring, KQL, log collection, and threat visualization.I configured this home lab on a Windows 11 virtual machine as the honeypot to observe multiple failed authentication attempts, along with analyzing security events from public services. 

## Technologies Used

-Microsoft Sentinel
-Microsoft Azure
-Windows 11 Virtual Machine
-Azure Log Analytics Workspace
-Azure Monitor Aganet (AMA)
-Kusto Query Language (KQL)
-Microsoft Sentinel Watchlists
-Microsoft Sentinel Workbooks
-Windows Event Viewer

## Implementation

### 1. Azure Honeypot Setup
Deployed a Windows 11 virtual machine and configured an isolated honeypot environment to look through unauthorized login attempts from users.

### 2. Security Log Collection
Configured a Log Analytics Workspace and connected Microsoft Sentinel using Azure Monitor Agent to collect Windows security events. Observed 35,000+ failed login events (Event ID 4625) in Windows Event Viewer.

### 3. Security Analysis with KQL
Used KQL to investigate failed authentication attempts, and filter through them.

```kql
SecurityEvent
| where EventID == 4625
| order by TimeGenrated desc
```

### 4. GeoIP Enrichment & Attack Map
Imported about 55,000 GeoIP records into a Sentinel watchlist and used KQL to connect source IP addresses with geographic locations.

### Key Takeaways
- Practiced KQL queries & GeoIP log enrichment.
- Visualized suspicious activity based on authentication using Microsoft Sentinel Workbooks.
- Analyzed various Windows security logs along with failed authentication attempts.
- Gained more hands-on experience to configure a cloud-based SIEM.


