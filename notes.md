######### step 1 to 4 #################

#### to find out Wifi driver 

ls /sys/class/net/wlan0/device/driver/module/drivers/


#### step 3 ###########

sudo wpa_supplicant -D nl80211 -i wlan0 -c network.conf


lenmor@lubuntu:~/SOEN421/krackattacks-test-ap-ft$ sudo wpa_supplicant -D nl80211 -i wlan0 -c network.conf
Successfully initialized wpa_supplicant
wlan0: CTRL-EVENT-SCAN-STARTED 

to delete currenly running wpa_supplicant
sudo rm /var/run/wpa_supplicant/wlan0




###### step 5 ##########

lenmor@lubuntu:~/SOEN421/krackattacks-test-ap-ft$ sudo wpa_cli -i wlan0
wpa_cli v2.1
Copyright (c) 2004-2014, Jouni Malinen <j@w1.fi> and contributors

This software may be distributed under the terms of the BSD license.
See README for more details.



Interactive mode

```

> 
> status
wpa_state=SCANNING
ip_address=192.168.1.102
p2p_device_address=00:25:d3:d4:e6:7a
address=00:25:d3:d4:e6:7a
uuid=e7879029-7e55-5a2e-8295-4bcf574abe31
<3>CTRL-EVENT-SCAN-STARTED 
<3>CTRL-EVENT-SCAN-RESULTS 
<3>WPS-AP-AVAILABLE 
> 
> 
<3>CTRL-EVENT-SCAN-STARTED 
<3>CTRL-EVENT-SCAN-RESULTS 
<3>WPS-AP-AVAILABLE 
> scan_results
bssid / frequency / signal level / flags / ssid
00:26:5a:f1:04:de	2437	-36	[WPA-PSK-CCMP+TKIP][WPA2-PSK-CCMP+TKIP][WPS][ESS]	dlink
40:65:a3:ad:34:2e	2412	-60	[WPA2-PSK-CCMP][WPS][ESS]	BELL436
b8:ec:a3:34:de:d0	2437	-43	[WPA-PSK-CCMP+TKIP][WPA2-PSK-CCMP+TKIP][WPS][ESS]	VIDEOTRON3670
48:ee:0c:2f:61:d0	2457	-52	[WPA-PSK-CCMP+TKIP][WPA2-PSK-CCMP+TKIP][WPS][ESS]	dlink-61D0
b4:75:0e:af:37:39	2412	-67	[WPA-PSK-CCMP+TKIP][WPA2-PSK-CCMP+TKIP][WPS][ESS]	DaTrapHouse
e4:6f:13:62:8e:08	2462	-59	[WPA-PSK-CCMP+TKIP][WPA2-PSK-CCMP+TKIP][WPS][ESS]	dlink-8E08
3c:90:66:53:3f:a4	2412	-73	[WPA2-PSK-CCMP][WPS][ESS]	EBOX-1524
10:fe:ed:71:1b:e1	2452	-78	[WPA2-PSK-CCMP][WPS][ESS]	FBIVAN
f0:82:61:47:51:19	2437	-80	[WPA2-PSK-CCMP][WPS][ESS]	BELL503
00:23:6a:ec:6c:54	2462	-82	[WPA-PSK-CCMP+TKIP][WPA2-PSK-CCMP+TKIP][ESS]	SmartRG7912
a0:1b:29:da:4f:8c	2437	-89	[WPA2-PSK-CCMP][WPS][ESS]	BELL280
02:1b:29:da:4f:8c	2437	-89	[WPA2-PSK-CCMP][ESS]	BELL280-V
b4:75:0e:af:37:3b	2412	-67	[ESS]	DaTrapHouse-guest
fa:8f:ca:9a:f4:9b	2412	-73	[ESS]	
40:f2:01:f3:9b:d7	2462	-87	[WPA2-PSK-CCMP][WPS][ESS]	BELL138
04:bf:6d:56:1d:ec	2462	-87	[WPA2-PSK-CCMP][WPS][ESS]	VIDEOTRON2393
44:e9:dd:50:72:3a	2462	-84	[WPA2-PSK-CCMP][WPS][ESS]	BELL469
88:a6:c6:83:3e:96	2412	-88	[WPA2-PSK-CCMP][WPS][ESS]	BELL844
1c:7e:e5:fa:16:32	2412	-80	[WPA-PSK-CCMP][WPA2-PSK-CCMP][WPS][ESS]	VIDEOTRON5900
2c:e4:12:a2:ad:87	2412	-87	[WPA2-PSK-CCMP][WPS][ESS]	BELL718
a0:e4:cb:f5:ab:a0	2437	-91	[WPA-PSK-CCMP+TKIP][WPA2-PSK-CCMP+TKIP][WPS][ESS]	VIDEOTRON6679
f0:82:61:49:31:4c	2437	-94	[WPA2-PSK-CCMP][WPS][ESS]	BELL341
90:72:82:f1:f4:66	2412	-90	[WPA2-PSK-CCMP][WPS][ESS]	BELL600
<3>CTRL-EVENT-SCAN-STARTED 

```

################################

try to connect to my wifi AP
fails at roaming wifi-ssid (dlink)


> roam 00:26:5a:f1:04:de

FAIL

