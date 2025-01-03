# Buidl by Hyperspec 

## A fully open source hyper spectral camera build for Raspberry Pi ## 

### Building the Front Lens ###

Insert the 35mm Lens in to "Part_02 Front Lens" and secure with screw 

Note you will need to edit the source file for part_02 if you use a different lens with greater aperture width 

### Building the Diffraction Grating ###

Using gloves to protect the grating cut a concentric rectangle to the same size as part_06 "diffraction grating" 

Secure with paper tape and avoid covering the transparent plastic of the diffraction grating  

### Build the HSI device ### 

Refer to https://github.com/Hyperspec-01/Buidl/blob/main/Install.jpg 

1) Part_01 Case. 2) Part_02 Front lens. 3) Part_03 Square aperture. 4) Part_04 Extension 1 of 2. 5) Part_05 Extension 2 of 2. 6) Part_06 Diffraction grating. 7) Part_07 Camera base. 8) Part_08 Seal extension. 9) Part_09 X extension. 10) Part_10 Lid. 11) RPI01 Raspberry Pi 5 . 12) RPI02 Raspberry Pi HQ Camera. 13) PS02 Power Supply Connector. 14) PS03 Power On/Off Switch. 15) +10 Macro 52 mm Lens. 16) LENS02 35 mm C Series.

### Software Installation ### 

Either via connected screen or via SSH you need to access your RPI 

First enable your camera 

```
raspi-config
```
choose "interfaces" then select "camera" and "enable" 

after reboot enter these commands to check image capture and video are working

```
raspistill -o example.jpg
```
```
raspivid -o videxample-h26-4
```




Once accessed install Hypraspcam 

Obtain your IP address

```
if config
```

Install the software, where the WiFi SSID and Password are asked for you can enter anything here but remember what you entered
```
sudo apt-get update

sudo git clone https://github.com/Hyperspec-01/HypRaspCam

cd HypRaspCam/

sudo chmod a+x install.sh

sudo ./install.sh
```
After reboot run 

```
sudo /etc/init.d/HypRaspCam stop
sudo /etc/init.d/HypRaspCam start
```
You should see a welcome message. You will also be able to see the SSID you set as an available WiFi Network on your phone or computer.

Then install SquareHSI. 

Firstly download this file and copy it in to the documents folder

https://github.com/Hyperspec-01/dotech.us_Deploy/blob/master/calibSquareHSI_Beta_1.AppImage

Now connect to the WiFi you created in the previous step

Now double click the downloaded file placed in the documents folder 

Choose "yes" for auto connect

Once the application has opened click on the "streaming" tab and then on the icon directly above the first tick box, this will create an image.













