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

# copy settings file and replace username and password
```
cd /etc/transmission-daemon
```
```
sudo wget https://raw.githubusercontent.com/bicklp/transmission-setup/master/settings.json
```
```
sudo nano /etc/transmission-daemon/settings.json
```
# edit the daemon file and replace transmission-daemon user with your own username
```
sudo nano /etc/init.d/transmission-daemon
```
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
