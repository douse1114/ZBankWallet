# ZBankWallet

Starting ZBank Wallet

The process for creating this blockchain wallet was pretty straight forward.  It started by creating 2 nodes and then intializing a genesis block.  This blockchain is simply a testnet and was created using Clique and is a Power of Authority network.  I used the puppeth function to create the genesis block and to name the network.  The information for the 2 nodes that I initialy created was saved into a txt file called 'Node Addresses.'  These addresses were important when it came time for activating the 2 nodes on the blockchain and sending transactions on the blockchain.  

In order to start making transactions with the ZBank Wallet, there are a few steps that need to be completed first.

1. Start by activating both nodes that were created.  In order to do this, it is necessary to have Geth Tools installed on the device you are using and these tools must me present in the folder that you are running the nodes in.  In this case all actions will be taking place in the Zbank folder.

2. In order to activate node 1, you will want to use the code './geth --datadir node1 --unlock 'SENDER ADDRESS NODE 1' --mine --minerthreads 1'
3. In order to activate node 2, you will want to use the code './geth --datadir node2 --unlock "SENDER ADDRESS NODE 2" --port 30304 --bootnodes "ENODE ADDRESS FROM NODE 1" --ipcdisable --allow-insecure-unlock'

4. Once both nodes are active and running, you will want to open the MyCrypto app (or any wallet app that you are using).  Once inside the app you will need to create a new network.  We have already created the network, we just need to link it to our MyCrypto app.  

5. In the bottom left corner of the MyCrypto app, there is an option to 'Change Network.'  In this option we will select the option to 'Add Custom Node.'  A new window will appear and you will want to enter the network name in the Node name section and change the network to 'Custom.'  We will keep the currecny as ETH and the Chain ID will be 333.  The url should be the default 'http://127.0.0.1:8545'

6. Now that the Zbank Network has been connected its time to upload the keystore for node 1 in order to begin processing transactions.

7.  Return to the home page and select 'Keystore File' at the bottom.  Upload the keystore file for Node 1 and enter the password that was created for the node and click unlock.

8. Once the wallet is unlocked, you will then be able to submit transactions for processing by entering the sending wallet address and the amount.  Then you will click send transaction.  You will see a pop up at the bottom of the screen that shows the transaction hash number.  Save this as a way of tracking the status of the transaction.  These transactions can be viewed under 'TX status' or they can be viewed on 'etherscan.com.'  You will also be able to see the account balance on the right hand side of the screen right below the account address.

Screenshots of the genesis block creation through puppeth can be found in the screenshots folder.  There are also additional screenshots of each step of the transaction process in the screenshots folder as well.

