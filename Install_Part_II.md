-- After Apache is installed --

#### Setting up Port Forwarding ####
A port forwarding needs to be set up on the router
- Name: -> the name you want to give this rule
- Internal Port: -> the port the server is listening | use command: sudo netstat -plnt
- External Port: -> what port do you want to use to listen externally 
(http:// request assume you requesting port 80 [if not specified]. https:// requests assume port 443)
- Protocol: -> Both would do
- IP Address: -> internal IP address of the device | use command: ifconfig (look for inet of wlan0 section)

!! Please Note: External IP is not accessible within local network. You need to use Internal IP to access it !!

#### Setting up DDNS (Dynamic DNS) ####
You'll need to set up DDNS. Two major providers:
- DynDNS - available on more devices, paid
- No-IP - free, chose to use this DDNS
Once you signed up, enter your information into DDNS section of your router

#### Creating User ####
Raspberry Pi default login times out, so you should make your own login to fix this problem\
$ sudo useradd -m <user>\
--Configuring Bash--\
Most likely, you bash is not configured, and you'll need to do this to be able to save command history etc.\
$ chsh -s /bin/bash\
or sudo execution\
$ sudo chsh <username> -s /bin/bash  
