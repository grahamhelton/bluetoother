# Bluetoother
## Usage
1. Install the bluetooth software
```bash
sudo apt-get -y install bluetooth bluez bluez-tools rfkill
```

2. Find out your device's hardware MAC Address
```bash
bluetoothctl
scan on
<turn your device on and look for it in the scan list>
scan off
exit
```
3. Edit the script and input your hardware's MAC address

4. Run the script
```bash
git clone https://github.com/grahamhelton/bluetoother 
chmod +x bluetoother
./bluetoother

-> Bluetooth service enabled, trying to connect you...
-> You're connected!
```

## Running with keypress in I3
bindsym $mod+shift+b exec /usr/bin/terminator -e /usr/bin/bluetoother

## References
https://computingforgeeks.com/connect-to-bluetooth-device-from-linux-terminal/
