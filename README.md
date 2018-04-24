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

**Add the following line to the bottom of the file**
```
rpcport=5004
```

**Then hold down `ctrl + 0` then hit `enter` then  `ctrl + x`**

**Now run the following line on the VPS**
```
venv/bin/python bin/sentinel.py
```

**After that run this command**
```
crontab –e 
```

**Then hit enter to use nano**

**At the end of the file add the following line **
```
* * * * *      cd /root/Sentinel-Demos/ && venv/bin/python bin/sentinel.py 2>&1 >> sentinel-cron.log
```

*Then hold down `ctrl and o` then hit `enter`, then hold down `ctl` and hit x*

*That' it just wait for a while and the WATCHDOG_EXPIRED status will disappear*
============================================================================================================




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

**Add the following to the bottom of the file**
```
rpcport=5004
```

*Then hold down `ctrl and o` then hit `enter` then hold down `ctrl and hit x`*

**Now run the folloing lines on the VPS**

```
nano /root/Sentinel-Demos/sentinel.conf
```

**Change the 4th line to the follow **

```
demos_conf=/root/.demos/demos.conf
```

**Then hold down `cttl and o` then hit `enter` then hold down `ctrl and hit x`**

**Run the following command**

```
venv/bin/python bin/sentinel.py
```

**After that run the following command**

```
crontab –e 
```

**Then hit enter to use nano**

**At the end of the file add the following line**

```
* * * * *      cd /root/Sentinel-Demos/ && venv/bin/python bin/sentinel.py 2>&1 >> sentinel-cron.log
```

*Then hold down `ctrl and o` then hit `enter` then hold down `ctrl and hit x`*
*That's it just wait a while and the WATCHDOG_EXPIRED status*
