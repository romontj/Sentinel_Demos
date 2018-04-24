# Demos Sentinel

*You only need this if you are running a masternode and getting WATCHDOG_EXPIRED*

# IF YOU USED THE ORIGINAL INSTALL METHOD ON THE WEBSITE USE THIS SECTION!!!# 

Run the following  commands on your linux VPS
Cd /root
```
wget https://raw.githubusercontent.com/growbtcprofits/Sentinel_Demos/master/Sentinel-Demos.tar.bz2 
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

**ADD THE FOLLING LINE TO THE BOTTOM OF THE FILE**
```
rpcport=5004
```

**THEN HOLD DOWN CTRL AND O  THEN HIT ENTER THEN HOLD DOWN CTRL AND HIT X**

**NOW RUN THE FOLLOWING LINE ON THE VPS**
```
venv/bin/python bin/sentinel.py
```

**AFTER THAT RUN THE FOLLOWING COMMAND**
```
crontab –e 
```

**THEN HIT ENTER TO USE NANO**

**AT THE END OF THE FILE ADD THE FOLLOWING LINE**
```
* * * * *      cd /root/Sentinel-Demos/ && venv/bin/python bin/sentinel.py 2>&1 >> sentinel-cron.log
```

**THEN HOLD DOWN CTRL AND O  THEN HIT ENTER THEN HOLD DOWN CTRL AND HIT X**
**THAT’S IT JUST WAIT A WHILE AND THE WATCHDOG ERROR WILL GO AWAY**
============================================================================================================

#IF YOU USED THE NEW INSTALL METHOD IN THE DISCORD USE THIS SECTION!!!

**Run the following  commands on your linux VPS**

```
Cd /root
```
```
wget --no-check-certificate https://host42.blockxplorer.info/Sentinel-Demos.tar.bz2 
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

**ADD THE FOLLING LINE TO THE BOTTOM OF THE FILE**
```
rpcport=5004
```

**THEN HOLD DOWN CTRL AND O  THEN HIT ENTER THEN HOLD DOWN CTRL AND HIT X**

#NOW RUN THE FOLLOWING LINEs ON THE VPS

```
nano /root/Sentinel-Demos/sentinel.conf
```

**CHANGE THE 4TH LINE TO THE FOLLOWING**

```
demos_conf=/root/.demos/demos.conf
```

**THEN HOLD DOWN CTRL AND O  THEN HIT ENTER THEN HOLD DOWN CTRL AND HIT X**

#RUN THE FOLLOWING COMMAND

```
venv/bin/python bin/sentinel.py
```

**AFTER THAT RUN THE FOLLOWING COMMAND**

```
crontab –e 
```

**THEN HIT ENTER TO USE NANO**

**AT THE END OF THE FILE ADD THE FOLLOWING LINE**

```
* * * * *      cd /root/Sentinel-Demos/ && venv/bin/python bin/sentinel.py 2>&1 >> sentinel-cron.log
```

**THEN HOLD DOWN CTRL AND O  THEN HIT ENTER THEN HOLD DOWN CTRL AND HIT X**
**THAT’S IT JUST WAIT A WHILE AND THE WATCHDOG ERROR WILL GO AWAY**
