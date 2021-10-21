# DigiPi with IQaudio Codec Zero

This page covers how to build a DigiPi with the IQaudio Codec Zero GPIO audio interface

Special thanks to Adam - SP3ADM for getting this configuration working! Thanks Adam!!!

IQaudio Codec Zero

https://www.raspberrypi.com/products/iqaudio-codec-zero/

IQaudio Codec Zero is a Raspberry Pi Zero-sized audio I/O HAT. It delivers bi-directional digital audio signals (I2S) between Raspberry Pi Zero and its onboard Dialog Semiconductor DA7212 codec. Codec Zero supports a range of input and output devices, from the built-in MEMS microphone to external mono electret microphones and 1.2W, 8Ω mono speakers.



Breakout PiZero addon

https://thepihut.com/collections/raspberry-pi-breakout-boards/products/breakout-pizero



Raspberry Pi OS Configuration Steps

THIS DOES NOT WORK!

Modify the config.txt file to enable the device overlay for the IQaudio Codec Zero

/boot/config.txt

`#dtparam=audio=on`
`dtoverlay=iqaudio-codec`



Verify functionality with Alsa Player:

pi@raspberrypi:~ $ aplay -l **** List of PLAYBACK Hardware Devices **** card 0: IQaudIOCODEC [IQaudIOCODEC], device 0: IQaudIO CODEC HiFi v1.2 da7213-hifi-0 [IQaudIO CODEC HiFi v1.2 da7213-hifi-0]  Subdevices: 1/1  Subdevice #0: subdevice #0

INSTEAD DO THIS:

edit /boot/config.txt

comment out line # dtparam=audio=off


edit /home/pi/
pcm.!default {

​    type asym

​    playback.pcm {

​        type plug

​        slave.pcm "dmixer"

​    }

​    capture.pcm {

​        type plug

​        slave.pcm "dsnooper"

​    }

}

pcm.dmixer {

type dmix

ipc_key 1024

slave {

pcm "hw:0,0"

rate 44100

period_time 0

period_size 1024

buffer_size 8192

}

}

pcm.dsnooper {

type dsnoop

ipc_key 816357492

ipc_key_add_uid 0

ipc_perm 0666

slave {

pcm "hw:0,0"

channels 1

}

}


sudo reboot now



Refer to the iqaudio repository on GitHub:

https://github.com/iqaudio/Pi-Codec



