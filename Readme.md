PoC for STF deployment on a single machine
===========
# Installation

* install docker
* install docker-compose
* clone this repo

# Usage
choose an IP your deployment should use, usually that will be the IP of your host.  
choose a secret to be used for inter-service authentication.  
Update the `.env` file accordingly

Run `docker-compose up -d --build`  
Point your browser to the IP you chose,  
login by providing any username and valid e-mail.


A little write-up on this setup:  
https://medium.com/@nikosch86/getting-started-with-automated-in-house-testing-on-android-smartphones-using-stf-dafecee4a8ee  
If you clap it will make me happy :)

ngrok for linux 32 bit: https://bin.equinox.io/c/4VmDzA7iaHb/ngrok-stable-linux-386.zip

##Put systemd service file in the right place and enable the service

sudo cp android-lab.service /lib/systemd/system/android-lab.service
sudo systemctl enable android-lab.service
