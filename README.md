# Threadmonitor
This script walks thread stacks of Event Log Service process (specifically svchost.exe) and identify Event Log Threads to monitor Log Service Threads. 
With this script splunk will be able to collect knowledge if event Log threads are killed even when the Event Log Service will appear to be running. 

I've edited the script of Halil DALABASMAZ in order to detect the Phant0m script which is also created by Halil DALABASMAZ (https://github.com/hlldz, https://twitter.com/hlldz).

# Usage

```
PS C:\> .\Threadmon.ps1

```

# Technical Details of Threadmon
You can change the last line in Threadmon.ps1 and change the function args to monitor threads by your choice.

Threadmonitoring(args)

Example args:
1. Monitor 1 servicename with 1 threadname
- args = "Servicename : Threadname"
2. Monitor multiple servicenames with a threadname
- args = "Servicename : Threadname, Servicename2 : Threadname2, etc..."
3. Monitor 1 Servicename with all threads
- args = "Servicename" <- to monitor all threads

	Also threadname is wildcarded before and after the given threadname

# Technical Details of Phant0m
https://artofpwn.com/phant0m-killing-windows-event-log.html

# Video of Phant0m
[![PoC Video](https://i.ytimg.com/vi/PF0-tZWCmpc/maxresdefault.jpg)](https://www.youtube.com/watch?v=PF0-tZWCmpc)


