# OSXNetwork

## setting static ipaddress from command line

-----------------
-----------------

## LIST ALL YOUR NETWORK DEVICES
```shell
cat /Library/Preferences/SystemConfiguration/NetworkInterfaces.plist
```
* locate -> plist -> dict -> key(interfaces) -> array -> dict > dict -> string
* in my case, it's "Thunderbolt Ethernet"


## SET IP ADDRESS 
```shell
networksetup -setmanual "$devicename" $ipaddr $netmask $gateway
```

## SET DNS
```shell
networksetup -setdnsservers "$devicename" 8.8.8.8 114.114.114.114
```
