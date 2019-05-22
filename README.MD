# Log Analytics WVD Query Examples

These are some example queries based on the WVD API logs as they existed last year during private preview.

The logs were collected via a custom powershell script that queries the WVD API on a schedule. At the time the logs could not be natively ingested into Log Analytics.

There are several areas, WVD specific logs, RemoteFX Performance counters and General Performance counters

## Remote FX Counters
To use the RemoteFX dashboard the below counters need to be added to Log Analytics perf counters. You can use PerfMon to find the exact name of any counter you want to add and add it. (https://www.systemcenterautomation.com/2018/11/custom-performance-counters-log-analytics/)

RemoteFX Graphics - Frames Skipped/Second - Insufficient Network Resources

RemoteFX Graphics - Frames Skipped/Second - Insufficient Server Resources

RemoteFX Graphics - Frames Skipped/Second - Insufficient Client Resources

RemoteFX Graphics - Source Frames/Second

RemoteFX Graphics - Frame Quality

RemoteFX Graphics - Graphics Compression ratio

Example RemoteFX Dashboard
![image](images/remotefx.png)

## WVD Information
![image](images/WVDinformation.png)

this dashboard provides count of hostpools, hosts, unique users and any errors users may have experienced during connection. The corresponding dashboard file is WVD information.omsview

## WVD Usage Time
![image](images/usagetime.png)

this dashboard provides count of Hostpools and usage time of host pools, hosts, usage of hosts by users and total usage time for users.

the corresponding dashboard file is time usage.omsview