# ESP-ARGB

<img width="1068" height="675" alt="image" src="https://github.com/user-attachments/assets/d5a9ef5c-5769-4dba-8647-415176f3e358" />
<img width="997" height="706" alt="image" src="https://github.com/user-attachments/assets/23d83739-c66c-4f24-ba80-6aab412ca778" />

## About it
It is a powerful small sized ARGB controller based on the ESP32 series microcontrollers and It allows for freedom of RGB lol, no more hassle with aftermarket controllers, while this integrates you PC RGB easily.
It is easy to make and very useful.

## Why?
MANY, I am talking many really, there are so many motherboards out there even new ones that DO NOT INCLUDE an integrated ARGB controller too, this seems to be a trivial problem at first, duh its just RGB, but I only knew the pain after buying a new case for my new PC build out of a very decent buisness motherboard that I had revived, the ASUS Prime B365M-C, I had no way to control or even simply light up the RGB int he front fans.
Imagine such a nice case with fans running with literally no RGB despite supporting it, its so bad to look at and its just a missed opportunity.
Yes there exists those ARGB controllers out there but either they are made out of chinesium or they really suck at controlling and you have no freedom of colors and what you wanna pick and no animations despite having argb control, its lost potential!!!!.
There exists such controllers that are bit good but they are from big box brands and give barely any control from their software.

So I set up to make a good argb controller that can live behind the motherboard tray or in the psu cover for PCs not having ARGB controllers built in, I mean even newer boards like H610M chipsets and stuff those cut down boards despite their black pcb color and their cool silkscreen, no ARGB controller :(

This also aims to solve the problem of using ur motherboard manufacturer's bloat they prepped up in like the win7 era that doesnt even run properly to control your ARGB bcs no other way to control!!

So I set out to make this, to atleast replace the ESP32 stuffed in a random carton just there and my sketchy botched up soldering of wires that may start a fire lmao.

<img width="709" height="945" alt="image" src="https://github.com/user-attachments/assets/bb323624-976e-4b0c-b053-9ffd59b68a7d" />

And give some light, lmao, to the people suffering without a argb controller with argb stuff heh.

## What does it have?
It has 3 distinct LED control channels in one channel you can plug 3 ARGB 3 pin connectors to control your fans in sync, I went with 3 since max ur gonna use 360mm stuff unless you are someome insane(atp use the manufacturer daisy chain ones hah).
The first two led channels can be connected to 3+3 rgb devices like fans and stuff, the last channel can only control and accept one argb and has only 1 connector since I intend it to be for addressable light strips!
And most importantly it uses an ESP32C3 and I intend to use WLED firmware for now, in the future may fork it, but this means we have WIFI control, 
Yes, wifi, it can either create its own wifi network and broadcast or if you dont want wifi interference, it can connect to your wifi network too and host its local website in that you can set a static ip and stuff ;)

It can also do cool animations and stuff like at startup after power for sometime it can do effects then change to another effect.
I rn use a solid effect after sometime of it on since I figure dynamic ones more distracting but you can customise it so many ways.

I don't wanna say all the features of WLED and show( I don't wanna flex lol and there are SOOOOOOO MANY FEATURES) so you can check out WLED!

https://kno.wled.ge/  :)

Btw, you can also program and have a link with it with a USB2.0 header in ur motherboard :) so no need to pull it out to do anything in software! It even includes serial debugging!!

## Main Hardware it uses
- ESP32C3 Microcontroller - The brains of the whole thing! Small and tiny but packs a punch!!
- A voltage regulator for the esp!!
- Other passive components like multiple film capacitors and mainly many bulk electrolytic caps near the RGB outputs for smoooooooooth power delivery hehe.
- Also, multiple 0Ohm linkages has been included in stuff like enabling serial debug, usb connection, connection to various light channels so you can disable the ones you don't use!

## How to build it and use!
Prerequisites: Have patience and a positive attitude!!!
oh and btw, have the pcb and components and case pieces on hand!!

1. Build the electronics! be patient and solder all the components to the pcb by seeing the schematic for the values of components!! Then assemble the case referencing the assembly on onshape!
2. Put it in your pc and connect it up! Connect the usb header to your usb 2.0 header on your motherboard
3. Power it up. If the magic smoke hasn't come out, your all good for now!!
4. Use a long bit dull pin or stick and press the reset button through the hole in the case and also connect the IO9 pin of the serial debug header to ground with the help of dupont jumpers while pressign the reset button and release the reset button and leave the IO9 pin connected to grounbd, it sends the esp into download mode!
5. If you have speakers or a headphone connected should hear a device connecting!
6. go to install.wled.me and click install, sleect the serial port of the esp it will show one as usb select that and install!
7. After install you are good to go and free to customise it all you want!!!!!

# Resources!!
## PCB layers
It is a 2 layer stackup

Top Layer:
<img width="1011" height="629" alt="image" src="https://github.com/user-attachments/assets/1be1b9ac-42b4-4d77-b94d-92715ffe518b" />
Bottom layer:
<img width="998" height="611" alt="image" src="https://github.com/user-attachments/assets/db856a5a-295e-4a85-afc7-c6443dd11e54" />

Both layers with copper areas:
<img width="1079" height="620" alt="image" src="https://github.com/user-attachments/assets/acf36196-1ee8-4b31-b273-02441e65f0c1" />
Without copper area both layers:
<img width="978" height="613" alt="image" src="https://github.com/user-attachments/assets/daf1dd11-43ef-4a2d-8d80-4019b7f558eb" />

All layers including silkscreen:
<img width="1109" height="614" alt="image" src="https://github.com/user-attachments/assets/807910e2-3635-4aaf-9e14-a37db0ea3698" />

## PCB 2D image:
<img width="1169" height="750" alt="image" src="https://github.com/user-attachments/assets/d5ffa718-5a4f-487d-8dee-462f19942e67" />
<img width="1183" height="743" alt="image" src="https://github.com/user-attachments/assets/acd5fe2b-a0f7-4557-9e56-9de3f36afd27" />

## PCB 3D images:
<img width="1008" height="675" alt="image" src="https://github.com/user-attachments/assets/002622aa-a289-4bfb-a366-f3d77af0690e" />
<img width="1118" height="603" alt="image" src="https://github.com/user-attachments/assets/b7781a19-bcb6-4d22-acf9-715f0dd2a839" />
<img width="1260" height="744" alt="image" src="https://github.com/user-attachments/assets/71360856-725d-452b-9081-b933c2be6f44" />

# Schematic
For building the electronics and for working on it generally you need the schematics.
[SCH_ESP-ARGB_2026-05-28.pdf](https://github.com/user-attachments/files/28345847/SCH_ESP-ARGB_2026-05-28.pdf)
<img width="1113" height="651" alt="image" src="https://github.com/user-attachments/assets/6d4c534f-0c70-42be-ad70-97ab71921672" />


## Case
The case consists of two main 3D printed pieces, the base piece and the top piece which will also enclose the PCB.
It is assembled by some clever techniques of using metal standoffs and bolts specifically to eliminate the need of complex fastening of parts while still giving good structural integrity!.

Here is the bottom piece alone
<img width="822" height="654" alt="image" src="https://github.com/user-attachments/assets/602598c0-7d21-4a22-8e76-440ac3169427" />
There are some cavities so I can further compress the whole build up and the pisn from the pcb wont collide and I dont need more space to clear them of anything.

Here is the lid top piece
<img width="901" height="662" alt="image" src="https://github.com/user-attachments/assets/f81c42ca-d923-4a19-997b-5f3f5d547154" />
<img width="638" height="653" alt="image" src="https://github.com/user-attachments/assets/b7dcb90b-1ff0-418f-bf23-4e1d8875029f" />

And it requires M2 6mm height female female standoff thing spaces lol and some bottomhead M2 screws of 4mm length.

Here is the final assembly of everything so can assemble it
Ignore the gap between the top case lid and bottom base, it will turn out actually a snug fit due to FDM printing.
<img width="1240" height="795" alt="image" src="https://github.com/user-attachments/assets/1a7306d8-76dd-4de1-954d-5b23c16255d7" />
<img width="1162" height="833" alt="image" src="https://github.com/user-attachments/assets/1a90260f-0ae6-43f1-8e5c-7d643b2b5c72" />
<img width="1115" height="729" alt="image" src="https://github.com/user-attachments/assets/eee0cf81-fffd-4305-8482-67bba2a985ec" />
<img width="1284" height="756" alt="image" src="https://github.com/user-attachments/assets/e9758414-91c3-4f27-b7b6-1c535967479f" />

Exploded views
Isometric
<img width="1125" height="873" alt="image" src="https://github.com/user-attachments/assets/ba802ffc-eda3-43bc-939c-1aa68a8b61a9" />
Dimetric
<img width="938" height="849" alt="image" src="https://github.com/user-attachments/assets/59f1805a-71df-4f57-9da2-6b47b4234ee4" />
Trimetric
<img width="933" height="824" alt="image" src="https://github.com/user-attachments/assets/23511170-1acf-40fd-9f5b-74684f4d72fa" />
Others
<img width="1098" height="862" alt="image" src="https://github.com/user-attachments/assets/8097ebbe-b9ca-4789-a936-efff725b5fc5" />
<img width="995" height="770" alt="image" src="https://github.com/user-attachments/assets/c40a652f-cf33-459f-a404-990268cd3b1c" />

Link to onshape document:
https://cad.onshape.com/documents/13ac6c5ca9052a6dc9df88c6/w/c9eeca4fde315684a9a5921a/e/b29c4cd3637df26137a43deb?renderMode=0&uiState=6a182a8d6ab1afd1b1dba4b8

## Bill Of Materials









