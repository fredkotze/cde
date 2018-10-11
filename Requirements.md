# General Requirements
Secure
* All communications are encrypted (HTTPS/ LDAPS etc)
* Authentication uses Single Sign-On (AD DS, LDAP, Certificates etc)
* Permissions are granular to allow both DXC and Customer access
* Audit trail shows data collection and any modification via Web and API interfaces

Resilient
* Minimize single points of failure
* Self healing / recovering of missed data
* Monitored for data collection and consistency

Flexible
* Configurable RU structures to meet contract billable structures
* Configurable data collection and retention timeframes including data granularity
* Agile development and DXC NSSR process allows for product improvements based on DXC and Client demand

Accessible
* Customer may replicate subsets of the  data for their own analysis
* DXC can access the data 24x7x52
* User interface via Web portal
* API interface via REST API and direct DB (Read Only) Query

# Billing Requirements (for example use case)
Billing RU Structures should be either (The most common seen to date):
* Component based for example: $/vCPU, $/vRAM, $/GB Storage Alloc, $/GB Storage Used, $/GB Network Transfer
* T-Shirt based for example: Small = 1 vCPU + 1GB vRAM, Medium = 2 vCPU + 2GB vRAM

Billing RU Structures can include additional breakdowns based on (IF the data is available to the collector):
* Operating System
* Application Functionality (Middleware, Web services, etc)
* Database
* Performance Tier / SLA / Location

Billing granularity and frequency:
* Granularity defined by the collector (e.g. 5 mins if vCenter Stats via PowerCLI)
* RUs billed per most granular OR Hourly OR Daily
* Cost-to-Date should must show the timeframe.
* Billing data archived in accordance to configured setting (e.g. 30, 60, 90 days etc)
