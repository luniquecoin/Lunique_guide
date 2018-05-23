# LUNIQUE

## Shell script to install a LUNIQUE Masternode on a Linux server running Ubuntu 16.04. Use it on your own risk.


## Installation:
### wget -q https://github.com/luniquecoin/Lunique_guide/releases/download/v3.0/luq_vps_masternode_hot_wallet.sh
### bash luq_vps_masternode_hot_wallet.sh


## Desktop wallet setup
## After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps for Windows Wallet

### 1. Open LUNIQUE Wallet.
### 2. Go to RECEIVE and create a New Address: MN1
### 3. Send 1000 LUQ to MN1.
### 4. Wait for 15 confirmations.
### 5. Go to Tools -> "Debug console - Console"
### 6. Type the following command: masternode outputs
### 7. Go to Tools -> "Open Masternode Configuration File"
### 8. Add the following entry:

## Alias Address Privkey TxHash Output_index
### * Alias: MN1
### * Address: VPS_IP:PORT
### * Privkey: Masternode Private Key
### * TxHash: First value from Step 6
### * Output index: Second value from Step 6

### 9. Save and close the file.
### 10. Go to Masternode Tab. If you tab is not shown, please enable it from: Settings - Options - Wallet - Show Masternodes Tab
### 11. Click Update status to see your node. If it is not shown, close the wallet and start it again. Make sure the wallet is un
### 12. Select your MN and click Start Alias to start it.


## Usage:
### luq-cli mnsync status
### luq-cli getinfo
### luq-cli masternode status #This command will show your masternode status

## Also, if you want to check/start/stop LUNIQUE , run one of the following commands as root:
### systemctl status Lunique #To check the service is running.
### systemctl start Lunique #To start Lunique service.
### systemctl stop Lunique #To stop Lunique service.
### systemctl is-enabled Lunique #To check whetether Lunique service is enabled on boot or not.