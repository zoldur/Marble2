# Marble
Shell script to install a [Marble Masternode](http://www.marblecoin.co/) on a Linux server running Ubuntu 16.04. Use it on your own risk.
***

## Installation
```
wget -q https://raw.githubusercontent.com/zoldur/Marble2/master/marble2_install.sh
bash marble2_install.sh
```
***

## Desktop wallet setup  

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps:  
1. Open the Marble Desktop Wallet.  
2. Go to RECEIVE and create a New Address: **MN1**  
3. Send **25000** MARCO to **MN1**. You need to send all 25000 coins in one single transaction.
4. Wait for 15 confirmations.  
5. Go to **Help -> "Debug Window - Console"**  
6. Type the following command: **masternode outputs**  
7. Open Windows Explorer and go to **%APPDATA%\Marbe** folder
8. Open/create masternode.conf
9. Add the following entry:
```
Alias Address Privkey TxHash TxIndex
```
* Alias: **MN1**
* Address: **VPS_IP:PORT**
* Privkey: **Masternode Private Key**
* TxHash: **First value from Step 6**
* TxIndex:  **Second value from Step 6**
10. Save and close the file.
11. Go to **Masternode Tab**. If you tab is not shown, please enable it from: **Settings - Options - Wallet - Show Masternodes Tab**
12. Click **Update status** to see your node. If it is not shown, close the wallet and start it again. Make sure the wallet is un
13. Select your MN and click **Start Alias** to start it.
14. Alternatively, open **Debug Console** and type:
```
masternode start-alias MN1
```
15. Login to your VPS and check your masternode status by running the following command. If you get **Status 9**, it means your masternode is active.
```
Marbled masternode status
```
***

## Usage:
```
Marbled masternode status  
Marbled getinfo
```
Also, if you want to check/start/stop **Marble2**, run one of the following commands as **root**:

```
systemctl status Marble2 #To check if Marble2 service is running
systemctl start Marble2 #To start Marble2 service
systemctl stop Marble2 #To stop Marble2 service
systemctl is-enabled Marble2 #To check if Marble2 service is enabled on boot
```  
***

## Donations

Any donation is highly appreciated

**MARCO**: MU52bvZwzAFGcQH3UpgU1fBi3wKNQm8PNs  
**BTC**: 3MQLEcHXVvxpmwbB811qiC1c6g21ZKa7Jh  
**ETH**: 0x26B9dDa0616FE0759273D651e77Fe7dd7751E01E  
**LTC**: LNZpK4rCd1JVSB3rGKTAnTkudV9So9zexB  