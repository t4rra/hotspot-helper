# Hotspot Helper
Fixes the lag spikes caused by windows hotspot when using wireless Virtual Reality streaming apps.

> This repository is no longer maintained! 

---

## Features
- Fixes the lag spikes caused by Windows Hotspot scanning
- Minimal setup
- Starts the hotspot and applies the fix

## Instructions
Setup the windows hotspot first. Go to the hotspot settings and configure the SSID/Password. Make sure to set the band to 5ghz, or you'll have a stuttery mess.

If it is your first time running the script, a first-time setup portion will list and ask you to select the wifi interface that will be used to create the hotspot.

It will then bring you into the main menu, where you can do one of 5 things: [1] Turn on hotspot with fix - [2] Restore AutoConfig - [3] Change Wireless Interface - [4] Exit - [5] Uninstall

## Windows Defender Flagged this as a Virus???
This program is open source, meaning that you can inspect and dissect the code yourself. If you're still wary, you can do what this script does manually below. 

### Manual Alternative
Make sure you're first conencted to a WiFi network. Specifications don't matter as long your WiFi chip/card supports WiFi 5ghz hotspots.

1. Setup your hotspot (mentioned above)
2. Turn on your hotspot
3. Disconnect from your connected WiFi network (if you want WiFi access, it might come at the cost of stutters/latency)
4. Run the command
```
netsh wlan set autoconfig enabled=no interface="[Network Interface]"
```
Replace [Network Interface] with the name of your network adapter (Circled in red below) ![Highlighted-Adaptername](https://user-images.githubusercontent.com/64815861/113248316-88433e00-9271-11eb-9c9a-3d76927cf991.PNG)

That's it! When you're done with VR, run the command below.
```
netsh wlan set autoconfig enabled=yes interface="[Network Interface]"
```
