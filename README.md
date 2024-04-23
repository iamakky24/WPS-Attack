# Brute-Forcing WPS Pins with Reaver in Kali Linux
Reaver performs a brute force attack against an access point’s WiFi Protected Setup pin number. Once the WPS pin is found, the WPA PSK can be recovered and alternately the AP’s wireless settings can be reconfigured.

### Tools Used

- Reaver is used to brute-force WPS PINs.

### Steps:
1: First, we should set up our Wireless device in Monitoring mode.
##### airmon-ng start wlan0
![1*F-ruSBGaG3us4925toikgA](https://github.com/iamakky24/Exploring-WiFi-Security/assets/73874888/fd5a7295-0274-4952-88b5-7540e46b4d7f)
#### You should notice for the device is set up in the Monitor mode wlan0mon.

2: Now we can see the BSSID of the devices that are near us to display all WPS-enabled WiFi networks.
##### airodump-ng wlan0mon
![1*kPltm6c1BRoUAfqXWEkMuw](https://github.com/iamakky24/Exploring-WiFi-Security/assets/73874888/99f2ec59-ab45-49cf-9866-04f487aaf933)
#### We have gathered all the required information

3: Now it's time to attack from Reaver.
##### reaver -i wlan0mon -b E8:65:D4:72:89:A1 -S -v
![1*Blc2FzxrLfHYVXGRRe6MLQ](https://github.com/iamakky24/Exploring-WiFi-Security/assets/73874888/e06af9cc-350e-417a-bbf9-235560558cee)
#### Now the tool will try all the possible pins to crack the WPS Pin of the target.

4: Once the correct pin found, It will display it.
![1*hqeCpmjSt8PqewImMSYY9A](https://github.com/iamakky24/Exploring-WiFi-Security/assets/73874888/958b39a4-5efa-4573-b0c4-2c44a63408a9)
#### As you can see, the Pin has been cracked.
