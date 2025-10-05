# Real-Time Threat Detection Stack(Wazuh & Suricata)
### Overview

## Wazuh Stack Configuration
- Ran Wazuh stack using custom docker compose file to assign custom IPs in my docker VLAN network

- Wazuh Stack

![Wazuh Containers](/Images/WazuhContainers.png "Wazuh Containers")
<br><br><br>
- Wazuh dashboard which diplays Alerts generated from agent and network monitoring logs over the last 24 hours
- Displays active and disconnected agents and other useful secuirty metrics such as Endpoint Security, Threat Intelligence, and Secuirity Operations

![Wazuh Dashboard](/Images/WazuhDashboard.png "Wazuh Dashboard")
<br><br><br>

- Installed 2 agents on my devices one is a Windows Gaming PC the other is an Linux Ubuntu Server I use to run services like my static portfolio site, photo cloud storage, and gaming servers.

![Endpoint Management](/Images/AgentsDashboard.png "Endpoint Management")
<br><br><br>

- This shows a closer look into the endpoint management where I selected my Ubuntu Server, it diplays things like Vulerability sorted by severity, compliance results, and secure configuration assessment scores.

![Endpoint Management](/Images/EndpointManagement.png "Endpoint Management")
- Windows PC to compare

![Windows Agent](/Images/windowsagent.png "Windows Agent")
<br><br><br>

- Intergrated Suricata alerts into SIEM dashboard by modiying config files

!["Config for Wazuh to ingest Suricata Logs"](/Images/wazuhlogsconfig.png "Config for Wazuh to ingest Suricata Logs")
!["suricata alerts in wazuh"](/Images/suricatawazuh.png "suricata alerts in wazuh")


## Suricata Configuration
- Installed Suricata service on my PFSense Firewall
- Created and configured the Interfaces for in Suricata to monitor all my VLAN networks but set up active blocking for the Server VLAN only(Disabled test networks)
![Suricata Interfaces](/Images/SuricataInterfaces.png "Suricata Interfaces")

- Suricata Alerts
![Suricata Alerts1 ](/Images/SuricataAlerts1.png "Suricata Alerts 1")
![Suricata Alerts 2](/Images/SuricataAlerts2.png "Suricata Alerts 2")
