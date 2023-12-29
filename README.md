# Bellscrition

# 1. First you need to install NODE JS on your computer. 👇👇👇 Use the link below to look for executables that will work on your computer.

How To install
```
https://nodejs.org/en/learn/getting-started/how-to-install-nodejs
```
Download from here
```
https://nodejs.org/en/download
```

After a successful installation and all requirements are met. send `node --version` it will output the version of your installed node js.


## 2. Minting Bellscription on Bell Mainnet is not yet possible using the marketplace or a front end.

### The best way to run it, is by using a volt to mint which can be gotten from the link below.

```
https://github.com/Nintondo/bellscoin/releases
```
* Copy link to your web browser and download the lastest release, current release is 2.0.0
* Choose the executable compatible with your system.
  - For Apple: download using `https://github.com/Nintondo/bellscoin/releases/download/2.0.0/bells-2.0.0-osx-unsigned.dmg`
  - For Windows x64 bit: download using `https://github.com/Nintondo/bellscoin/releases/download/2.0.0/bells-2.0.0-win64-setup-unsigned.exe`

After download, and installation, *DO NOT OPEN THE APP*

Navigate using your file explorer on you computer to

```
C:\Users\$user\AppData\Roaming\
```
* where `C:` is the hardrive label
* where `$user` is your computer name.
 - create a folder and name it `Bells`
 - create a file `bells.conf` using your note pad and put in this data 👇👇
   
```
rpcuser=user # change this to your username
rpcpassword=pass # change this to your preferred password
server=1
rpcport=19918
rpcbind=0.0.0.0
rpcallowip=127.0.0.1
par=8
fallbackfee=0.001
rpcworkqueue=16
rpcthreads=4
maxconnections=64
txindex=1
```
THEN YOU CAN RUN THE BELLS CORE WALLET APPLICATION AND SAVE YOUR KEYS
  * Go to file (located at the top left)
  * select backup wallet.

# 3. clone the inscriptor/minter on your cli
Copy this in your command prompt or node command prompt and clone bells inscriptor repo from git hub
```
git clone https://github.com/ordinals-wallet/bellscriptions.git
```
then, change directory into the repo
```
cd bellscriptions
```

This will install requirements necessary for the packages to function.
- create a `.env` file
  - by using any text editor of your choice. I used Vim
    - Do ```vi .env``` and copy this data into it.
```
NODE_RPC_URL=http://127.0.0.1:19918/
NODE_RPC_USER=user # To the username you used you used on bells.conf
NODE_RPC_PASS=pass # To the password you used you used on bells.conf
TESTNET=false
```

Install the packages in the repo by using this command.

```
npm install
```
After a successful installation. send 👇👇👇

```
node . wallet new
```
*This will create a wallet and create a file name ```.wallet.json``` in the directory, this contains your wallet address and private-key
so guide it jealously.*

copy the wallet address on screen and fund it using this exchange. [Nonkyc](https://nonkyc.io?ref=658eefbd0936b99a9500bac4)
you can fund as low as $2 $BELLS.

Next, use the command to sync the wallet with your local node running.

```
node . wallet sync
```

You can vi or nano into your ```.wallet.json``` copy your privatekey and download [Bells Wallet](https://github.com/Nintondo/extension/releases/tag/0.0.7)
import the wallet to track transactio coming and out of the wallet when you make the inscription commands.

# 4. Time to Mint
* create a .txt file using Vim. ```vim bells.txt``` copy and input the inscription data into the buffer.
```
{"p":"bel-20","op":"mint","tick":"BELL","amt":"1000"}
```
*press esc, : , x and enter. to save the file*


* create a .txt file using Vim. ```vim pepe.txt``` copy and input the inscription data into the buffer.
```
{"p":"bel-20","op":"mint","tick":"PEPE","amt":"1000"}
```
*press esc, : , x and enter. to save the file*

* * create a .txt file using Vim. ```vim nook.txt``` copy and input the inscription data into the buffer.
```
{"p":"bel-20","op":"mint","tick":"nook","amt":"500000000"}
```
*press esc, : , x and enter. to save the file*

# 5. Minting using the CLI
* To mint the above data you need to use the line command in this format
```
node . mint <Wallet you want to mint on> <name of file.txt> <amount of times to mint>
```

* To mint nook max mint 5 times, all i need to do is.
```
node . mint BNMNxjJMrWfqouAoiwTmTGK9qy5rFqat8G nook.txt 5
```

Good Luck, wait for more update and data to inscribe.
Leave a star and follow.


