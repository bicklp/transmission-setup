# transmission-setup
Setup Transmission on Raspberry Pi

```
sudo apt-get update -y
```
```
sudo apt-get install transmission-daemon -y
```
```
sudo service transmission-daemon stop
```

# copy settings file
```
cd /etc/transmission-daemon
```
```
sudo wget https://raw.githubusercontent.com/bicklp/transmission-setup/master/settings.json
```
```
sudo nano /etc/transmission-daemon/settings.json
```
# add own username by replacing debian-transmission
```
sudo nano /etc/init.d/transmission-daemon
```
# this is need to get permission to NAS

# take ownership of the files
```
sudo chown bicklp:bicklp -R /etc/transmission-daemon
```
```
sudo chown bicklp:bicklp -R /var/lib/transmission-daemon
```
# update the service to start delayed
```
sudo update-rc.d transmission-daemon defaults 92
```
```
sudo service transmission-daemon start
```
