# INFORMATION

This repository is for binary files for rpcapd, this tool allows wireshark on a different computer to remotely connect 
and live stream packets being seen or generated by the remote device.

I did not in most cases compile the file(s) but I have tested they function.
With this tool a raspberry pi can become an excellant remote diagnostic tool allowing for example in-line tracing configurations
or even configurations where the RPi will call home and join a VPN and provide remote visibility.

I have personally used both of these configurations in my day job and found it to be really useful during the covid-19 lockdown.
I hope this will assist others too.

# INSTALATION
There is no real installation as such simple download the file rpcapd.arm in this repo and then save it on your RPi.
The directory I normally place it is in /usr/bin/ as that directory is on the command path, for sake of ease I will assume in this README that you too are going to use this directory.
I normally rename the file from rpcapd.arm to simply rpcapd on linux this can be done using the following 
command assuming you are in the same directory as the downloaded file and want to place in the aformentioned directory:
*sudo mv rpcapd.arm /usr/bin/rpcapd*

Next in order to execute the file we need to add the permissions
*sudo chmod +x /usr/bin/rpcapd*

# RUNNING
To see the help information type *rpcapd -h* at the command line.
my normal way to run is to use
*rpcapd -d -n*

The two options i use most ofter are:
-d  start as a daemon
-n  do not authenticate device connecting (wireshark does not support authentication.

# SIGNING OFF
I hope this assists someone.

Caio
Paul

