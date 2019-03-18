
##**1.Set up Master Node**

**Prerequisite**

- Operating System: Ubuntu 16.04 64-bit or higher. Should be facing internet directly with public IP & without NAT

- Tools: Git, Docker, Docker Compose

- Network Ports

Following network ports need to be open for the nodes to communicate.

8545  TCP - RPC <br>   
30303 TCP/UDP - XDC

**How to Setup Masternode ?**

**0. Install Git**

* Check whether git is preinstalled.

    > git --version

If present, output will be something like git version 2.17.1. In this case, go to step a.Otherwise follow the below steps.

- sudo apt update
- sudo apt install git
- git --version

* Configure Git.

- git config --global user.name "Your Name"
- git config --global user.email "youremail@domain.com"

**a. Clone repository**

Run the following commands on your terminal.

- git clone [https://github.com/XinFinOrg/XinFin-Node.git](https://github.com/XinFinOrg/XinFin-Node.git)
- cd XinFin-Node

The git clone command will create a new folder XinFin-Node. cd XinFin-Node command changes the current directory to XinFin-Node

**b. Install docker & docker-compose**

       sudo ./install\_docker.sh

The above command will install docker and docker-compose for you.

**c. Update .env file with details**

* Copy a env.example file from XinFin-Node directory and name it as a .en
* Open .env file and edit values for following

- INSTANCE_NAME : A display name of your masternode
- CONTACT_DETAILS : Your Email Id

![overview](/assets/xinfin-node.png)

![overview](/assets/masternode-.env.png)


**d. Start your Node**

        sudo docker-compose -f docker-services.yml up -d

This will start a Masternode and connect to a XinFin Testnet.

You should be able to see your node listed on this page: [XinFin Network](https://www.xinfin.network) (Make sure, you are connected to XinFin Testnet. If not, switch to Tesnet on top right corner.)

Your coinbase address can be found in xdcchain/coinbase.txt file.

![overview](/assets/masternode-listing.png)

##**2. Stake XDC**

  **Create XDC Wallet**

      > Visit http://xinfin.network/#webWallet and Click on create a new wallet.
      > you can create use a web wallet or download eWallet app from Google Play Store.
      > Create an account
      > Store your private key at a safe place (Hardware wallet is recommended)

![overview](/assets/xinfin_wallet.png)


   **Buy XDC**

     > get your free XDC to use on XinFin Testnet
     > Visit XinFin TestNet Faucet http://xinfin.network/#getTestXDC.
     > Add your wallet address created in step 2.b and request XDC

![overview](/assets/masternode-faucet.png)

##**3. Upload KYC**

    > Visit http://xinfin.network/#masternode
    > Upload a notarized kyc

##**4. Become a Candidate**

Add your account address and click on "Become a Candidate" to become a masternode. You must have minimum 10 Million XDC in your account. Once your candidature is accepted, your stake of 10 Million XDC is locked.

![overview](/assets/1.png)


##**5. Factoring Process**

In a typical factoring on infactor.io, there are 3 parties involved. Supplier, Buyer and Financier. Supplier is a starting point. Supplier uploads Invoice, Buyer validates invoice and Financier factors on invoice.

- Register on http://infactor.io.

Choose your role(Supplier, Buyer, Financier)

On successful registration, a wallet account is automatically created for you.


Note : To register, you must have uploaded KYC, staked XDC and you are a part of XDC Network by running a masternode. In case of any malicious activity, the staked XDC will be frozen.

![overview](/assets/2.png)

- Supplier uploads invoice details and related documents.

![overview](/assets/3.png)

- Buyer verfies invoice authenticity and approves/rejects invoice.

![overview](/assets/4.png)

- Supplier selects an approved invoice for factoring. All financiers on the platform receive new factoring notification. Financer sends a factoring proposal along with related documents to supplier. The proposal includes interest rate/month and the upfront payment percent of total invoice amount.

![overview](/assets/5.png)

- Supplier approves the factoring proposal and the notification is sent to the selected financier. 
Financier pays first payment to supplier as per factoring criteria.


Note : To transfer amount, a user has to load the amount into a wallet. A deposit functionality is present in user profile section.

![overview](/assets/6.png)

- Buyer pays invoice amount to financier. A financier pays final payment(by deducting fees) to supplier.

Fee calculation is done on the basis of Interest Rate (as per factoring criteria) and payout date. If Buyer pays invoice amount earlier to financier, fees will be less and vice versa. The fees calculation is done on the smart contract.

- Financier and Supplier can rate each other.

![overview](/assets/8.png)
