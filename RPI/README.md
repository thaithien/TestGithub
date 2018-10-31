

# Some Notes for my RPI

## How to install RPR OS without screen
see http://raspberrypi.stackexchange.com/questions/15192/installing-raspbian-from-noobs-without-display

## Node module to send out public IP address


## Set up transmission torrent client
see http://www.techjawab.com/2014/08/how-to-install-transmission-on.html
```shell
--Step 1
sudo apt-get update
sudo apt-get install transmission-daemon
Step 2
Create required directories on your NAS storage (path to storage is assumed as /media/NASDRIVE)
mkdir -p /media/NASDRIVE/Torrent_inprogress
mkdir -p /media/NASDRIVE/Torrent_complete

Step 3
Permissions
Transmission by default runs with user "debian-transmission", as it is recommended not to change this due to security reasons. In our setup the NASDRIVE has the permission set as 770 for pi : pi. Thus we will add user "debian-transmission" to "pi" group to give rwx access on our NASDRIVE. You can go ahead and modify this step as per your security requirement, but just make sure your torrent download directories are having rw access for "debian-transmission" user.
sudo usermod -a -G pi debian-transmission

Step 4
Configure Transmission
While most of the parameters are self explanatory in the conf file, you can use the file given below, except for modify the parameters download-dir, incomplete-dir, rpc-username, rpc-password 
Note: rpc-password will automatically converted to hashstring on saving the file 
sudo nano /etc/transmission-daemon/settings.json
Step 5
Reload Transmission
Do not restart, It overwrites the configuration file in that case
sudo service transmission-daemon reload 

Step 6
Open web browser and hit http://your_raspberry_pi_IP:9091
Enter the user id and password you've configured, and viola!
```


## Set up node
see http://www.andrewconnell.com/blog/setup-node-js-on-raspberry-pi-2-b

wget http://node-arm.herokuapp.com/node_latest_armhf.deb
sudo dpkg -i node_latest_armhf.deb
node -v
curl -L https://npmjs.com/install.sh | sh



## How to run my nodejs application on boot

- Make /etc/rc.local, add your command line there
- 


# Pi-Hole

Link [Pi-Hole Forum](https://discourse.pi-hole.net/)
