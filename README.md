![Example-Logo](https://i.imgur.com/wtdV9uw.png)
# WCF Coin Guide
Shell script to install a [WCF Coin Masternode](https://www.worldcryptoforumcoin.com/) on a Linux server running Ubuntu 16.04 Use it on your own risk.



***
## v1.1 >> v2.2 Update setup guide:
```
wget https://github.com/worldcryptoforum/WCF-Guide/releases/download/v2.2/wcf-v1.1-v2.2-update.sh
bash wcf-v1.1-v2.2-update.sh
```


**If the update script does not work properly after the update, delete the server and install it with the v2.2 installation script.**
**(When you delete the wallet, never delete the “wallet.dat” file. If the file is erased, Your coin may disappear.)**



***
## v2.2 Installation:
```
wget https://github.com/worldcryptoforum/WCF-Guide/releases/download/v2.2/wcf-v2.2-vpn-setup.sh
bash wcf-v2.2-vpn-setup.sh
```
***
## Desktop wallet setup

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps for Windows Wallet

1. Open the WCF Coin Coin Desktop Wallet.
2. Go to RECEIVE and create a New Address: **MN1**
3. Send **1000** **WCF Coin** to **MN1**.
4. Wait for 15 confirmations.
5. Go to **Tools -> "Debug console - Console"**
6. Type the following command: **masternode outputs**
7. Go to  **Tools -> "Open Masternode Configuration File"**
8. Add the following entry:

```
Alias Address Privkey TxHash Output_index
```
* Alias: **MN1**
* Address: **VPS_IP:PORT**
* Privkey: **Masternode Private Key**
* TxHash: **First value from Step 6**
* Output index:  **Second value from Step 6**
9. Save and close the file.
10. Go to **Masternode Tab**. If you tab is not shown, please enable it from: **Settings - Options - Wallet - Show Masternodes Tab**
11. Click **start** all in the masternodes tab
12. If it does not start at 11, follow the instructions below. Go to wallet - Tools - Debug console - Console - Type to **masternode start-alias MN1**
13. Next, go to our **Discord channel** for detailed instructions: [Discord](https://discord.gg/mCgYKbb)

***

## Usage:
```
worldcryptoforum-cli getinfo
worldcryptoforum-cli masternode debug
```
Also, if you want to start/stop **WCF Coin** , run one of the following commands as **root**:

`start : ./worldcryptoforumd`

`stop : ./worldcryptoforum-cli stop`
