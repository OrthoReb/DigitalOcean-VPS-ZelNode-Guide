***

<p align="center">
  <img width="860" height="315" src="https://imgur.com/tQQkMPn.png/860/315">
</p>

***

**This guide will assist you in setting up a ZelNode on a DigitalOcean VPS running Ubuntu 18.04.5 x 64**

**If you require further assistance contact the support team on [Discord](https://discord.gg/szN9yZ) or [Telegram English](http://t.me/zelcash) / [Chinese](http://t.me/zelcashcn) / [Russian](http://t.me/zelcashru)**
***
## Requirements
1) **ZEL Collateral (10K Basic / 25K Super / 100K BAMF)**
2) **VPS running Linux Ubuntu 18.04** (benchmark requirements can't be guranteed for servers that the team hasn't tested)
3) **Controller wallet (ZelCore or ZelCash Swing Wallet)**
4) **SSH client such as [Putty](https://www.putty.org/)**
***
## Contents
* **Section A : Preparing ZelCore Wallet**
* **Section B : Creating [DigitalOCean](https://www.digitalocean.com/) VPS**
* **Section C : Downloading and Installing [Putty](https://www.putty.org/)**
* **Section D : Connecting VPS and Installing ZelNode Script**
* **Section E : Connecting and Starting ZelNode**

***

## Section A: Preparing ZelCore Wallet
***Step 1***
* **Open your ZelCore wallet and choose 'Test Coin'** 

![Example-OS](https://imgur.com/kCb62vH.png)

***

***Step 2***
* **Click on 'Full Node' and then 'Launch Full Node'**

![Example-OS](https://imgur.com/YTUksqm.png)

***

**Step 3***

* **'Launch Test Coin' when prompted** 

![Example-OS](https://imgur.com/E3NbrdO.png)

***

***Step 4***
* **Go into Tools after wallet is 100% synced**

![Example-OS](https://imgur.com/cCReOTt.png)

***

***Step 5***
* **Open ZelNodes Management**

![Example-OS](https://imgur.com/ApVw4AU.png)

***

***Step 6***
* **Setup ZelNodes**

![Example-OS](https://imgur.com/eGZlrRC.png)

***

***Step 7***
* **Backup addresses**

![Example-OS](https://imgur.com/xdQYGOP.png)

***

***Step 8***
* **Set automatic logout to never**

![Example-OS](https://imgur.com/g8niH0e.png)

***

***Step 9***
* **Continue to the next step after your zelcash.conf info is generated**

![Example-OS](https://imgur.com/RTfsbRM.png)

***

***Step 10***
* **Choose which type of ZelNode you are going to run**

![Example-OS](https://imgur.com/Q3a4MPV.png)

***

***Proceed to the next section, but leave your ZelCore wallet open so that we can continue where we left off***

***

## Section B: Creating DigitalOcean VPS
***Step 1***
* **Register at [DigitalOcean](https://m.do.co/c/c9c22684c5db) (use this [referral link](https://m.do.co/c/c9c22684c5db) to receive a $100 credit that's good for 2 months)**

***

***Step 2***
* **After you have your account setup go [here](https://cloud.digitalocean.com/droplets?i=8fe2ca&preserveScrollPosition=false) to create your ZelNode droplet**

![Example-OS](https://imgur.com/WYFdC1j.png)

***

***Step 3***
* **Choose server type: 'Ubuntu 18.04'**
![Example-OS](https://imgur.com/4hM9ugU.png)

***

***Step 4***
* **Choose Droplet (Basic/Super/BAMF)**

![Example-OS](https://imgur.com/sVaawzt.png) ![Example-OS](https://imgur.com/1hAuT2T.png) ![Example-OS](https://imgur.com/Yc3Wm7q.png)

***

***Step 5***

![Example-Location](https://imgur.com/hjmZiaf.png)

***

***Step 6***

![Example-OS](https://imgur.com/qlYDSVn.png)

***


## Section C: Downloading and Installing Putty

***Step 1***
* **Download Putty [here](https://www.putty.org/)**

***

***Step 2***
* *Select the correct installer depending upon your operating system, and follow the install instructions** 

![Example-Putty Installer](https://imgur.com/U7eaNSh.png)

***

## Section D: Connecting VPS and Installing ZelNode Script

***Step 1***
* **Copy your VPS IP (located within Droplets tab)**
![Example-DO](https://imgur.com/8YWMNxW.png)

***

***Step 2***
* **Open the Putty terminal and fill in the "Host Name" box with the IP address of your VPS**

![Example-PuttyLogin](https://imgur.com/gMkd6fs.png)

***

***Step 3***
* **Once you hit 'Open' a security alert will be prompted (click yes)**

![Example-RootPassEnter](https://imgur.com/z0N2AMT.png)

***

***Step 4***
* **Type "root" as the login/username**

![Example-Root](https://imgur.com/DumQVJ5.png)

***

***Step 5***
* **Copy the root password that DigitalOcean emailed you**

***

***Step 6*** 
* **Paste the password into the Putty terminal by right clicking (it will not show the password so just press enter)**

![Example-RootPassEnter](https://imgur.com/TqeHV2C.png)

***

***Step 7*** 
* **Change password for root (UNIX password same as Step 5)**

![Example-RootPassEnter](https://imgur.com/vSXtaaG.png)

***

***Step 8***
* **Adduser to secure your VPS, by adding a new username so you aren't running everything as root**  

* **Run the command below and use a username that you want associated with this server ('whodatbamf1' is an example, you need to generate your own username)** 

`adduser YOURUSERNAME`

![Example-Bash](https://imgur.com/HJwb8tT.png)

***

***Step 9***

* **You will then need to make a new password associated with your new username.  Hit 'Enter' for the next 5 lines after your new password has been set, then 'Y' to save your information.**

![Example-Bash](https://imgur.com/suf0D9Y.png)

***

***Step 10***

* Grant sudo permissions for your adduser by running the command below to activate it

`usermod -aG sudo YOURUSERNAME`

* Switch to your new adduser with the following command

`su YOURUSERNAME`

![Example-Bash](https://imgur.com/qYIK75u.png)
***

***Step 11***
* Paste the code below into the Putty terminal then press enter

`sudo wget https://raw.githubusercontent.com/Goose-Tech/ZelNodeInstall/master/zelnode_install.sh && sudo chmod u+x zelnode_install.sh && sudo ./zelnode_install.sh`
***

***Step 12***
* Enter your new username that we made in Step 8

![Example-installing](https://imgur.com/vuMGJ1s.png)
***

***Step 13***
* Go back to your ZelCore wallet and enter your IP address

![Example-installing](https://imgur.com/aPvgKI0.png)
***

***Step 14***
* Name your ZelNode 

![Example-installing](https://imgur.com/YspTi4J.png)
***

***Step 15***
* Save your private key that is generated in ZelCore and enter when prompted on your VPS 

![Example-installing](https://imgur.com/It7FQjW.png)
***

***Step 16***
* Confirm IP, enter 'N' that you're not running for mainnet and enter private key from Step 15

![Example-installing](https://imgur.com/WFXTDpg.png)
***

***Step 17***
* Proceed to the next step while you wait for the install (this will take a few mins)

***Step 18***
* Go to the ZelCash block explorer `https://testnetnodes.zel.cash/blocks`

![Example-installing](https://imgur.com/liBNF5O.png)
***

***Step 19***
* Press CTRL-C in your VPS when the blocks match explorer in Step 19

![Example-installing](https://imgur.com/CqD1Kqa.png)
***

***Step 20***
* Activate your ZelNode

![Example-installing](https://imgur.com/xyPmofR.png)

* Successfully started 

![Example-installing](https://imgur.com/GGpcyFA.png)

***(IT WILL TAKE 15 CONFIRMATIONS FOR YOUR ZELNODE TO SHOW UP IN 'MY ZELNODES')***
***

***Step 21***
* Run the following command in Putty to confirm that your ZelNode is showing 'Status 4'

`sudo zelcash-cli getzelnodestatus`

![Example-installing](https://imgur.com/nj76J7D.png)

* You can also view your ZelNode on the block explorer `https://testnetnodes.zel.cash/zelnodes`
***(IT WILL SHOW UP AS 'PRE_ENABLED' UNTIL THERE ARE 15 CONFIRMATIONS)***

![Example-installing](https://imgur.com/SkGqa6D.png)
***

***CONGRATULATIONS AND THANK YOU FOR BEING A PART OF THE COMMUNITY!!!!!!!!!!!!!***

***


