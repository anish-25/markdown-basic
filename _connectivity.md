#Connectivity, Staging & Production

The TerraPay system is hosted on AWS across regions where available. A partner connecting to the TerraPay system will connect to the nearest AWS region which is in close proximity to the partner network. The TerraPay system is hosted as primary (PR) site, disaster recovery (DR) site and geographic redundancy (GR) site. TerraPay will connect to partner DR and GR systems to ensure service is not impacted when primary site is down.

Partner systems are allowed access to the TerraPay network through a secure VPN tunnel. This will be set up in both the PR and DR setups. Each of these will have two VPN tunnels, active and standby.

All the API interfaces between TerraPay and partner will be on HTTPS. TerraPay's inbound APIs are protected with a CA issued SSL certificate. Partner must also secure a CA issued SSL certificate for all APIs.

Partners integrate with TerraPay on the EIG (External Interface Gateway) which is hosted in the DMZ (De-Militarized Zone) of the TerraPay network. Access to all inbound and outbound APIs will be provided on the TerraPay staging system for integration testing. After API testing and validations are done then partners will be migrated to live production systems.