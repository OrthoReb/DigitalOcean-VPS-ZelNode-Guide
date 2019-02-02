***

<p align="center">
  <img width="860" height="300" src="https://imgur.com/nViX296.png/860/300">
</p>

***
**This guide will assist you in setting up a ZelNode on a DigitalOcean VPS running Ubuntu 16.04.5 x 64 (Use at your own risk)

**If you require further assistance contact the support team on [Discord](https://discord.gg/szN9yZ) or [Telegram English](http://t.me/zelcash) / [Chinese](http://t.me/zelcashcn) / [Russian](http://t.me/zelcashru)

***
## Requirements
1) **ZEL Collateral (10K Basic / 25K Super / 100K BAMF)**
2) **VPS running Linux Ubuntu 16.04** (benchmark requirements can't be guranteed for servers that the team hasn't tested)
3) **Controller wallet (ZelCore or ZelCash Swing Wallet)**
4) **SSH client such as [Putty](https://www.putty.org/)**
***
## Contents
* **Section A**: Creating the VPS within [DigitalOCean](https://www.digitalocean.com/)
* **Section B**: Downloading and installing [Putty](https://www.putty.org/)
* **Section C**: Connecting to the VPS and installing the ZelNode script via Putty
* **Section D**: Preparing the local wallet
* **Section E**: Connecting & starting your ZelNode
***

## Section A: Creating your DigitalOcean VPS
***Step 1***
* Register at [DigitalOcean](https://m.do.co/c/c9c22684c5db) (use this [referral link](https://m.do.co/c/c9c22684c5db) to receive a $100 credit that's good for 2 months)
***

***Step 2***
* After you have your account setup go [here](https://cloud.digitalocean.com/droplets?i=8fe2ca&preserveScrollPosition=false) to create your ZelNode droplet
![Example-OS](https://imgur.com/WYFdC1j.png)
***

***Step 3***
* Choose server type: Ubuntu 16.04
![Example-OS](https://imgur.com/aRpRv7X.png)
***

***Step 4***
* Choose Droplet (Basic/Super/BAMF)

![Example-OS](https://imgur.com/sVaawzt.png) ![Example-OS](https://imgur.com/1hAuT2T.png) ![Example-OS](https://imgur.com/Yc3Wm7q.png)
***

***Step 5***

![Example-Location](https://imgur.com/hjmZiaf.png)
***

***Step 6***
![Example-OS](https://imgur.com/qlYDSVn.png)
***


## Section B: Downloading and Installing Putty

***Step 1***
* Download Putty [here](https://www.putty.org/)
***

***Step 2***
* Select the correct installer depending upon your operating system, and follow the install instructions 

![Example-Putty Installer](https://imgur.com/wqfWyvg.png)
***

## Section C: Connecting to the VPS & Installing the ZelNode Script via Putty

***Step 1***
* Copy your VPS IP (located within Droplets tab) 
![Example-DO](https://imgur.com/8YWMNxW.png)
***

***Step 2***
* Open the Putty terminal and fill in the "Host Name" box with the IP address of your VPS

![Example-PuttyLogin](https://imgur.com/gMkd6fs.png)
***

***Step 3***
* Once you have hit enter it will open a security alert (click yes)

![Example-RootPassEnter](https://imgur.com/z0N2AMT.png)
***

***Step 4***
* Type "root" as the login/username

![Example-Root](https://imgur.com/S0fcGzm.png)
***

***Step 5***
* Copy the root password (check your email)
***

***Step 6*** 
* Paste the password into the Putty terminal by right clicking (it will not show the password so just press enter)

![Example-RootPassEnter](https://imgur.com/65jWobg.png)
***

***Step 7*** 
* Change password for root (UNIX password same as Step 5)

![Example-RootPassEnter](https://imgur.com/vSXtaaG.png)
***

***Step 8***
* Adduser to secure your VPS, by adding a new username so you aren't running everything as root.  
* Run the command below and use a username that you want associated with this server ***('whodatbamf1' is an example, you need to generate your own username).***  

`adduser YOURUSERNAME`

![Example-Bash](https://imgur.com/HJwb8tT.png)

***

***Step 9***

* You will then need to make a new password associated with your new username.  Hit 'Enter' for the next 5 lines after your new password has been set, then 'Y' to save your information.

![Example-Bash](https://imgur.com/suf0D9Y.png)

***

***Step 10***

* The final step is granting sudo permissions for your adduser, and running the command below to activate it***('whodatbamf1' is an example, you need to use your username)***

`usermod -aG sudo YOURUSERNAME`

* Now you will close your Putty terminal and log back with your new username and password that we made above 

![Example-Bash](https://imgur.com/qYIK75u.png)

* ***KEEP YOUR NEW USERNAME AND PASSWORD IN A SAFE PLACE.  THIS WILL BE HOW YOU LOG IN FROM NOW ON.***
***

***Step 11***
* Paste the code below into the Putty terminal then press enter

`sudo wget https://raw.githubusercontent.com/dk808zelnode/zelnode-testnetscript/master/testnet_script.sh && sudo chmod u+x testnet_script.sh && sudo ./testnet_script.sh`
***

***Step 12***
* Sit back and wait for the install (this will take a few mins), and have a txt file ready to save info from Step 11
***

***Step 13***
* After the install is complete you will need to save this info for your controller wallet
![Example-installing](https://imgur.com/95iQQB2.png)
***

## Section D: Preparing your ZelCore wallet using [trial123Zel](https://github.com/zelcash/zelcash/wiki/ZelNode-Setup-Guide-%7C-ZelCore-Full-Node)'s guide


