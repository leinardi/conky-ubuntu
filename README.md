# Yet another conkyrc file for Ubuntu

![enter image description here](https://github.com/leinardi/conky-ubuntu/blob/master/res/preview.png)

## Features ##
### General info ###
 - Ubuntu release version and codename 
 - Kernel release and machine name
 - CPU usage (percentage)
 - RAM usage (absolute and percentage)
 - Swap usage (absolute and percentage)
 - Uptime
 - Current time
 
### CPU info ###
 - CPU model
 - CPU frequency
 - CPU cores (including virtuals)
 - CPU usage chart
 - CPU cores temperature
 - CPU cores usage
 - CPU load (averages for the past 1, 5, and 15 minutes)
 
### Processes info ###
 - Tasks (total and running)
 - Top 4 task by CPU usage
 - Top 4 task by Memory usage
 
### Hard Disk info ###
 - Disk IO chart
 - Up to 3 partitions usage (absolute and percentage)
 
### Network info ###
 - Local IP (wlan, eth0, eth1)
 - Wlan signal strength
 - Wlan SSID
 - Public IP
 - Ping

## Configuration ##
### Hard Disk info ###
It is possible to customize the names and the partitions to show in the Hard Disk info section by changing the code between line [106](https://github.com/leinardi/conky-ubuntu/blob/master/conkyrc-775px#L106) and line [113](https://github.com/leinardi/conky-ubuntu/blob/master/conkyrc-775px#L113).
For example, if you want to replace the `Dati` partition with a different one, you need to change the name of the Partition in line [112](https://github.com/leinardi/conky-ubuntu/blob/master/conkyrc-775px#L112) and replace all the occurrences of the mount point `/media/Dati_ext4` inside the configuration file with your new mount point path.

### Network info ###
Since version 15.04 Ubuntu is using the [Predictable Network Interface naming](https://www.freedesktop.org/wiki/Software/systemd/PredictableNetworkInterfaceNames/) for all the network interfaces. This means that instead of having  traditional interface naming scheme ("eth0", "eth1", "wlan0", ...) we now have a scheme similar to biosdevname's ("enp7s0", "enp8s0", "wlx00147c67caec", ...).

To correctly display the Network information of your interfaces you need to replace the specific values of my PC with your specific values.

The following command provides a list of all your specific interfaces: `ip link show`
