# rhel-guide

### Connect to internet

On VM Virtual Box Manager right click on the virtual machine and click settings.  
Click Network, set ...  
Attached to: Bridged Adapter  
In Advanced  
set ...  
Promiscuous Mode : Allow VMs  
check Cable Connected  
vi /etc/sysconfig/network-scripts/ifcfg-enp0s3  
and add below code
```
...
DNS1=8.8.8.8
DNS2=8.8.4.4
# Note this was set to no
ONBOOT=yes  
```
then...  
```
sudo reboot now
```
