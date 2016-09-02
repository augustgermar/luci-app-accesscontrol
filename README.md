# luci-app-accesscontrol
Original Version is Here:
https://github.com/k-szuster/luci-access-control
This has been updated and tested to work with CC, DD and Trunk,
Whereas the original is tested only with BB and CC.

The previous version also required custom edits to 
 /openwrt/feeds/luci/contrib/package/luci-addons/Makefile

However now all you need to do to test and install is to add a link to the files in feeds.conf. 

Note:
--Scheduler uses military (24 hour) time
--Kernel Time is in UTC. 
--uses iptables kerneltz switch, which is not functioning in CC.
--that is why in CC you have to set your schedule in UTC , regardless of system time. 
--more details on iptables kernel modules and timezone here:
http://whirlysworld.blogspot.com/2013/08/blocking-internet-at-specific-times.html


This is a known bug in CC, it is not the version of iptables but something missing from the kernel. 
In DD/trunk the scheduler uses system time properly. 

