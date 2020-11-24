---
layout: page
title: "Velas Node Setup"
date: 2020-11-23 11:00:00 +0800
categories: guides velas-node
---

# ![](https://github.com/dexempower/https-dexempower.github.io-velas/blob/main/assets/logos/Logo1xxxhdpi.png?raw=true)  Welcome to Velas Blockchain User Guides :books:

![](https://github.com/dexempower/https-dexempower.github.io-velas/blob/main/assets/logos/Logo%20Lettersxxxhdpi.png?raw=true)
## DESKTOP & WEB GUIDE :computer:

# GUIDE TO NODE SETUP

### **TABLE OF CONTENTS**


**PREREQUISITES** 

**STEP 1. VELAS WALLET - GENERATING AND COPYING THE SCRIPT**

**STEP 2. RUNNING THE SCRIPT ON A DEDICATED SERVER/VPS**

**[METHOD 1]**   FROM WINDOWS 10 USING A GRAPHICAL ENVIRONMENT – WinSCP + PuTTY 

_CHECK YOUR VPS/DEDICATED SERVER PUBLIC IP_

_CONNECT USING WINSCP AND CREATE THE SCRIPT FILE_

_CONNECT WITH YOUR VPS OR DEDICATED SERVER USING PUTTY_

_ASSIGN PERMISSIONS AND RUN THE SCRIPT_

**[METHOD 2]** FROM LINUX / OSX/WINDOWS USING COMMAND LINE

_CHECK YOUR VPS/DEDICATED SERVER PUBLIC IP_

_LOG IN VPS/DEDICATED SERVER_

_CREATE NODE SCRIPT_

_ASSIGN PERMISSIONS AND RUN THE SCRIPT_ 

**STEP 3. VELAS WALLET – APPLYING TO BE CANDIDATE**
  
### INTRODUCTION
- This manual contains a step-by-step guide for Velas node setup.
- All active nodes are candidates, currently, 19 validators are chosen per epoch, based on the list of candidates.
- When a node is chosen as a validator, it and all its delegates will receive a reward (staking) at the end of the epoch.
- Balance, uptime, stability, or computer power are some of the parameters that the Velas AI analyzes to decide who will be the next validators in the network.
 
 - Any user on the Velas network can configure and run a node.
 - For more details, please visit our [website](http://www.velas.com/) and consult the [technical paper](https://velas.com/VELAS-Technical_Paper.pdf).

### PREREQUISITES

&nbsp; &nbsp; <img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/TaskManager.png?raw=true" width="100">

- 1,000,000 VLX or more.
- Basic Linux knowledge.
- VPS/ Dedicated server configuration knowledge.
- Predisposition to keep the node and its runtime environment always up to date and running.

### MINIMUM  REQUIREMENTS FOR VPS/DEDICATED SERVER

&nbsp; &nbsp; &nbsp; &nbsp; <img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/Hardware.png?raw=true" width="80">

- Linux (Ubuntu LTS/Debian/Centos)
- 10 or 8 Cores CPU (Xeon E5 2630-e3, Xeon E5 2630-e4, Xeon 4114, or AMD EPYC 7282)
- 16 GB RAM
- 250 GB Disk Space
- Unlimited traffic
- 1 Gb Ethernet port

## VELAS WALLET - GENERATING AND COPYING THE SCRIPT
**a)** Access the wallet (https://wallet.velas.com) using your ¨PIN / Password¨ and scroll to the left menu and select Staking > Node.

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/Pin.png?raw=true"  width="700"> <img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/NodeMenu.png?raw=true">

**b)** From this menu, pressing ¨Generate¨ will show the script that we will have to run 24/7 on our local, VPS, or dedicated server, copy the script to your clipboard.

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/Generate.png?raw=true"> <img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/CopyButton.png?raw=true">


## RUNNING THE SCRIPT ON A DEDICATED SERVER OR VPS

**c)** The next step is to paste the script generated in the wallet in our Linux VPS/Dedicated Server already preconfigured. There are different ways to do this, also depending on what operating system you use.

### [METHOD 1] FROM <img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/Windowslogo.png?raw=true" width="20"> WINDOWS 10 USING A GRAPHICAL ENVIRONMENT – WinSCP + PuTTY

**CHECK YOUR VPS/DEDICATED SERVER PUBLIC IP**

- From your VPS/Dedicated server control panel, check your public IP to login in your machine, in my case is 185.247.117.38, also look at your username, and your password, you will need it next.

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/VPS1.png?raw=true"> <img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/VPS2.png?raw=true">

**CONNECT USING WINSCP AND CREATE THE SCRIPT FILE**

- Connect with your VPS/Dedicated server using [WinSCP](https://winscp.net/) <img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/WINSCP.png?raw=true" width="80">

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/WINSCPSETUP.png?raw=true">

>File protocol: SFTP
>
>Host name: Your VPS/Dedicated server IP
>
>Port number: 22
>
>User name: Your VPS/Dedicated server username
>
>Password: Your VPS/Dedicated server password

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/LocalRemote.png?raw=true">

- Access your Velas wallet/account containing 1M VLX or more, copy the script as we show you in <STEP 1> if you haven't done it yet right click on the right side of  WinSCP, and create a new file as shown in the image.

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/Newfile.png?raw=true">

- Name it, for example, ¨node.sh¨ and click ¨OK¨, using ¨¨Ctrl+V¨ paste the script and save this file using the icon indicated with the red arrow.

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/Newok.png?raw=true"> <img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/Newctrlv.png?raw=true" width="800">

You can close WinSCP, we are done with this program.

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/WINSCPCLOSE.png?raw=true" width="800">

**CONNECT WITH YOUR VPS OR DEDICATED SERVER USING PUTTY**

- Open PuTTY and connect with your VPS/Dedicated server, you will need the IP, the SSH port (22), your username and your login password for your VPS or dedicated server, click ¨Open¨ and enter your username and password to log in via SSH.

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/VPSCONNECT.png?raw=true"> <img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/VPSLOGIN.png?raw=true">

**ASSIGN PERMISSIONS AND RUN THE SCRIPT**

- After login,  move to the directory where you have created the file ¨node.sh¨ using ¨cd¨ command, in the example, we have the file in the root directory¨/¨, you can check this using ¨ls¨ and you should be able to see the file:

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/LS.png?raw=true">

- Assign execution permissions to the file using the command ¨chmod + x¨
<chmod +x node.sh>

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/CHMOD.png?raw=true">

- Execute the script using ¨nohup¨ or ¨screen¨  to prevent it from stopping when you log out:
<nohup ./node.sh &>	

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/NOHUP.png?raw=true">

- Using ¨htop¨  you should be able to see the script running in the background, you can identify it as ¨Velasblockchain¨ <htop>

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/HTOP.png?raw=true">

- **The system clock must be synced**
- **Port 30304 should be visible from the outside**
- **Our node must be completely synchronized with the blockchain**

### [METHOD 2] FROM <img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/LINUX.png?raw=true" width="20"> LINUX / OSX <img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/OSX.png?raw=true" width="20"> USING COMMAND LINE

**CHECK YOUR VPS/DEDICATED SERVER PUBLIC IP**

- From your VPS/Dedicated server control panel, check your public IP to login in your machine, in my case is 185.247.119.44, also look at your username, and your password, you will need it next.

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/VPS3.png?raw=true">

**LOG IN VPS/DEDICATED SERVER**

- Open a terminal window and log in to your VPS / Dedicated Server using ¨ssh¨ command and your server IP, user & password.
<ssh user@IP> In this example: <ssh root@185.247.119.44>

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/SSHROOT.png?raw=true">

- If it asks you if you want to establish a connection, type ¨Yes¨ and press enter, then you will have to write your password to access your server and press enter again.

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/SSHYES.png?raw=true">

- You will see the command line of your server:

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/SSHloged.png?raw=true">

**CREATE NODE SCRIPT**

- Create the document that will contain the script, we can name it as we wish, for example, "node sh". For this we write the following command:
<nano node.sh>

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/NanoNode.png?raw=true">

- Right-click to paste the script that we should have copied in <STEP 1>

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/NanoPaste.png?raw=true">

- Press ¨Ctrl+X¨ to save the file:

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/NanoX.png?raw=true">

- Press ¨Y¨ to confirm:

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/NanoConfirm.png?raw=true">

**ASSIGN PERMISSIONS AND RUN THE SCRIPT**

- Assign execution permissions to the file using the command ¨chmod + x¨
<chmod +x node.sh>

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/CHMOD.png?raw=true">

- Execute the script using ¨nohup¨ or ¨screen¨  to prevent it from stopping when you log out:
<nohup ./node.sh &>	

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/NOHUP.png?raw=true">

- Using ¨htop¨  you should be able to see the script running in the background, you can identify it as ¨Velasblockchain¨ <htop>

<img src="https://github.com/dexempower/dexempower.github.io-velas/blob/main/assets/node/HTOP.png?raw=true">

- **The system clock must be synced**
- **Port 30304 should be visible from the outside**
- **Our node must be completely synchronized with the blockchain**
























































# WORK IN PROGRESS


