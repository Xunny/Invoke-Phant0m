# Threadmonitor
This script walks through thread stacks of the Event Log Service process (more specifically svchost.exe) with the purpose to monitor the Event Log Service Threads. Moreover, with this script, you'll be able to gain extra knowledge of the Event Log threads when they're killed or suspended. 

I've edited the Phant0m script which is created by Halil DALABASMAZ (https://github.com/hlldz, https://twitter.com/hlldz).

# Usage

```
PS C:\> powershell -exec bypass
PS C:\> .\Threadmon.ps1

```
NOTE: Run Powershell as Administrator

# Technical Details of Threadmon
You can change the last line in Threadmon.ps1 and change the function arguments to monitor threads by your choice.

Threadmonitoring(args)

Example args:
1. Monitor 1 servicename with 1 threadname
<br />args = "Servicename : Threadname"
2. Monitor multiple servicenames with a threadname
<br />args = "Servicename : Threadname, Servicename2 : Threadname2, etc..."
3. Monitor 1 Servicename with all threads
<br />args = "Servicename"

NOTE: threadname is already wildcarded before and after the given threadname

OUTPUT: JSON

# Technical Details of Phant0m
https://artofpwn.com/phant0m-killing-windows-event-log.html

# Video of Phant0m
[![PoC Video](https://i.ytimg.com/vi/PF0-tZWCmpc/maxresdefault.jpg)](https://www.youtube.com/watch?v=PF0-tZWCmpc)


