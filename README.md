# FastWay Masternode install (Ubuntu 16.04)
***

## Installation
```
wget -q https://raw.githubusercontent.com/GordenPirs/mninstall/master/install.sh
bash install.sh
```

## Desktop wallet setup

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps:  
1. Open the FastWay Desktop Wallet.  
2. Go to RECEIVE and create a New Address: **MN1**  
3. Send **25000** FAW to **MN1**. You need to send all 25000 coins in one single transaction.
4. Wait for 15 confirmations.  
5. Go to **Settings -> Console"**  
6. Type the following command: **createmasternodekey**
7. Type the following command: **getmasternodeoutputs**
8. Go to  **C:\Users\username\AppData\Roaming\Fastway**
9. Add the following entry:
```
127.0.0.1:3344 privatekey transaction index
```
* Alias: **MN1**
* Address: **VPS_IP:PORT**
* Privkey: **Masternode Private Key**
* TxHash: **First value from Step 6**
* Output index:  **Second value from Step 6**
9. Save and close the file.
10. Go to **Masternode Tab**. If you tab is not shown, please enable it from: **Settings - Options - Wallet - Show Masternodes Tab**
11. Click **Update status** to see your node. If it is not shown, close the wallet and start it again. Make sure the wallet is un
12. Select your MN and click **Start Alias** to start it.
13. Alternatively, open **Debug Console** and type:
```
masternode start-alias MN1
```
14. Login to your VPS and check your masternode status by running the following command:.
```
FastWay-cli masternode status
```
***

## Usage:
```
fastway-cli getmasternodestatus  
fastway-cli getinfo
```
Also, if you FastWay to check/start/stop **FastWay**, run one of the following commands as **root**:

```
systemctl status fastway.service #To check if fastway service is running  
systemctl start fastway.service #To start fastway service  
systemctl stop fastway.service #To stop fastway service  
systemctl is-enabled fastway.service #To check if fastway service is enabled on boot  
```  
***
