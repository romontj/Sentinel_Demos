# Demos Sentinel

*You only need this if you are running a masternode and getting WATCHDOG_EXPIRED*

# If you used the origial method on the website follow this section!!!# 

Run the following  commands on your linux VPS
Cd /root
```
wget https://raw.githubusercontent.com/growbtcprofits/Sentinel_Demos/master/Sentinel-Demos.tar.bz2
```
``` 
tar -xvf Sentinel-Demos.tar.bz2
```
```
sudo apt-get -y install python-virtualenv virtualenv
```
```
cd /root/Sentinel-Demos/
```
```
virtualenv ./venv
```
```
./venv/bin/pip install -r requirements.txt
```
```
nano /root/.demoscore/demos.conf
```

**Check and make sure it like the conf below **
```
rpcuser=username here (u can change to anything you want )
rpcpassword=password here (u can change to anything u want )
listen=1
server=1
daemon=1
txindex=1
rpcport=5004
masternode=1
logtimestamps=1
masternodeprivkey=Your_Mn_Genkey(change this to your masternode genkey) 
externalip=140.82.39.51:5005
addnode=18.188.99.190
addnode=18.188.220.201
addnode=13.59.221.246
addnode=52.15.63.29
```

**Then hold down `ctrl + 0` then hit `enter` then  `ctrl + x`**

**Now run the following line on the VPS**
```
/home/demos-cli stop
```
```
/home/demosd -daemon
```
```
cd /root/Sentinel-Demos/ && venv/bin/python bin/sentinel.py
```

**Wait for it to sync use `/home/demos-cli mnsync status` to make sure it fully synced and has "AssetName": "MASTERNODE_SYNC_FINISHED" **

**After that run this command**
```
crontab -e
```

```
select `2`
```

**Then hold down `ctrl and o` then hit `enter`, then hold down `ctl and hit x`**

**That' it just wait for a while and the WATCHDOG_EXPIRED status will disappear**

```
```

# If you used the new install method in the discord use this section!!

**Run the following  commands on your linux VPS**

```
Cd /root
```
```
wget https://raw.githubusercontent.com/growbtcprofits/Sentinel_Demos/master/Sentinel-Demos.tar.bz2
```
```
tar -xvf Sentinel-Demos.tar.bz2
```
```
sudo apt-get -y install python-virtualenv virtualenv
```
```
cd /root/Sentinel-Demos/
```
```
virtualenv ./venv
```
```
./venv/bin/pip install -r requirements.txt
```
```
nano /root/.demos/demos.conf
```

**Check and make sure it like the conf below **
```
rpcuser=username here (u can change to anything you want )
rpcpassword=password here (u can change to anything u want )
listen=1
server=1
daemon=1
txindex=1
rpcport=5004
masternode=1
logtimestamps=1
masternodeprivkey=Your_Mn_Genkey(change this to your masternode genkey) 
externalip=140.82.39.51:5005
addnode=18.188.99.190
addnode=18.188.220.201
addnode=13.59.221.246
addnode=52.15.63.29
```

**Then hold down `ctrl + 0` then hit `enter` then  `ctrl + x`**

**Now run the following line on the VPS**
```
/home/demos-cli stop
```
```
/home/demosd -daemon
```
```
cd /root/Sentinel-Demos/ && venv/bin/python bin/sentinel.py
```

**Wait for it to sync use `/home/demos-cli mnsync status` to make sure it fully synced and has "AssetName": "MASTERNODE_SYNC_FINISHED" **

**After that run this command**
```
crontab -e
```

```
select `2`
```

**Then hold down `ctrl and o` then hit `enter`, then hold down `ctl and hit x`**

**That' it just wait for a while and the WATCHDOG_EXPIRED status will disappear**