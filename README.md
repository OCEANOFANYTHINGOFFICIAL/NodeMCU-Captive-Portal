<p align="center" width="100%">
    <img width="60%" align="center" src="https://oceanofanythingofficial.github.io/NodeMCU-Captive-Portal/src/Thumbnail.png"/>
	<br>
    <div align="center">
      <img alt="GitHub code size in bytes" src="https://img.shields.io/github/languages/code-size/OCEANOFANYTHINGOFFICIAL/NodeMCU-Captive-Portal?style=flat">
  <img alt="GitHub Repo Version" src="https://img.shields.io/badge/Version-1.0.0.0-brightgreen?style=flat">
  <a target="_blank" href="LICENSE" title="License: MIT"><img src="https://img.shields.io/badge/License-MIT-blue.svg"></a>
  <a href="https://www.linux.org/" title="Go to Linux homepage"><img src="https://img.shields.io/badge/OS-Linux-blue?logo=linux&logoColor=white" alt="OS - Linux"></a>
  <a href="https://www.apple.com/macos/" title="Go to Apple homepage"><img src="https://img.shields.io/badge/OS-macOS-blue?logo=apple&logoColor=white" alt="OS - macOS"></a>
  <a href="https://www.microsoft.com/" title="Go to Microsoft homepage"><img src="https://img.shields.io/badge/OS-Windows-blue?logo=windows&logoColor=white" alt="OS - Windows"></a>
	<a href="https://oceanofanythingofficial.github.io/NodeMCU-Captive-Portal" title="Go to GitHub Pages homepage"><img src="https://img.shields.io/badge/Hosted_with-GitHub_Pages-blue?logo=github&logoColor=white" alt="Hosted with GH Pages"></a>
	<img  src="https://img.shields.io/badge/maintained-yes-blue"  alt="maintained - yes">
	<div><a href="https://oceanofanythingofficial.github.io/NodeMCU-Captive-Portal/" title="Go to project documentation"><img src="https://img.shields.io/badge/view-Documentation-blue?style=for-the-badge" alt="view - Documentation"></a></div>
   </div>
</p>

## Disclaimer
This project is for testing and educational purposes. Use it only against your own networks and devices. I don't take any responsibility for what you do with this program.

## About this project
WiFi captive portal for the NodeMCU (ESP8266 Module) with DNS spoofing.

This project can steal any Wi-Fi passwords in simple way. It uses a fake update page to get the password from the user. You just need to edit the Wi-Fi SSID name and the password will be posted to the ESP8266.

The built-in LED will blink 5 times when a password is posted.

<b>Warning!</b> Your saved passwords will **not** disappear when you restart/power off the ESP8266.

<b>Note:</b> If you want to see the stored passwords go to "**192.168.4.1**<a>/pass</a>". For changing the SSID, go to "**192.168.4.1**<a>/ssid</a>"



# Screenshots

<table>
  <tr>
    <th>192.168.4.1/index</th><br>
    <th>192.168.4.1/post</th><br>
    <th>192.168.4.1/pass</th><br>
    <th>192.168.4.1/ssid</th><br>
  </tr>
  <tr><br>
    <td>This is the main page. Here the user will write his password and send it.</td><br>
    <td>This is the post page. The user will be redirected here after posting the password.</td><br>
    <td>This is where the attacker can retrieve all the passwords that has been posted.</td><br>
    <td>Here the attacker can change the SSID name of the Access Point on the go.</td><br>
  <tr><br>
    <td><img width="200px" src="src/1_Index_2.png" title="index"></td><br>
    <td><img width="200px" src="src/2_Post.png" title="post"></td><br>
    <td><img width="200px" src="src/3_Pass.png" title="pass"></td><br>
    <td><img width="200px" src="src/4_ssid.png" title="ssid"></td><br>
  </tr>
</table>



# Installation (ESP8266 Flasher - Easy way)

1. Download <a href="https://github.com/nodemcu/nodemcu-flasher"><b>ESP8266 Flasher</b></a>.

2. Download the [NodeMCU-Captive-Portal.ino.bin](https://github.com/OCEANOFANYTHINGOFFICIAL/NodeMCU-Captive-Portal/raw/main/NodeMCU-Captive-Portal/build/esp8266.esp8266.generic/NodeMCU-Captive-Portal.ino.bin) file.

3. Open the ESP8266 Flasher and select the Node MCU port

<img width="80%" src="src/1_port_selection.png">

4. Then, go to the config tab and select the .bin file you've just downloaded.

<img width="80%" src="src/2_file_selection.png">

5. Finally, go back to the first tab and press "Flash"

6. Your Node MCU is ready!


# Installation (Arduino IDE)

1. Open your <a href="https://www.arduino.cc/en/main/software">Arduino IDE</a> and go to "File -> Preferences -> Boards Manager URLs" and paste the following link:
``http://arduino.esp8266.com/stable/package_esp8266com_index.json``

2. Go to "Tools -> Board -> Boards Manager", search "esp8266" and install esp8266

3. Go to "Tools -> Board" and select your board

4. Download and open the sketch "<a href="https://github.com/OCEANOFANYTHINGOFFICIAL/NodeMCU-Captive-Portal/blob/main/NodeMCU-Captive-Portal/NodeMCU-Captive-Portal.ino"><b>NodeMCU-Captive-Portal.ino</b></a>"

5. You can optionally change some parameters like the SSID name and texts of the page like title, subtitle, text body etc.

6. Upload the code into your board.

7. You are done!

