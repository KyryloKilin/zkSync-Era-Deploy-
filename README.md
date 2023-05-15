# zkSync-Era-Deploy-
##zkSync Era | Deploy 

###Requirements
The following are minimum requirements to Deploy:

```
CPU: 2-cores
RAM: 4GB of memory
Storage: 30GB of disk space
Network: 10 Mbps of upload and download bandwidth
Software: Linux
```

###Server Preparation
```
sudo apt-get update && sudo apt-get install -y
apt install curl -y
curl -sL https://deb.nodesource.com/setup_16.x -o /tmp/nodesource_setup.sh
sudo bash /tmp/nodesource_setup.sh
sudo apt-get install -y nodejs
sudo apt-get install vim
```

###Preparing for Deploy
```
npm init -y
npm install --save-dev hardhat
npm install -g npm@9.6.2
npx hardhat
```
```
Press Create a TypeScript project
Press Enter
Press Y 3 times
```

![image](https://github.com/KyryloKilin/zkSync-Era-Deploy-/assets/83702309/f6256bd8-b70a-497f-9185-0c80f1129bf4)

```
mkdir greeter
cd greeter
npm init -y
npm add -D typescript ts-node @types/node ethers@^5.7.2 zksync-web3@^0.14.3 @ethersproject/hash @ethersproject/web hardhat @matterlabs/hardhat-zksync-solc @matterlabs/hardhat-zksync-deploy
vim hardhat.config.ts
```
```
Press Esc
Write :wq
Press Enter
```
```
mkdir contracts
mkdir deploy
vim contracts/Greeter.sol
```
```
Press Esc
Write :wq
Press Enter
```
```
npx hardhat compile
vim deploy/deploy.ts
```

###Change <WALLET-PRIVATE-KEY> in the code to your own private key
  
```  
Paste the modified code into the console

Press Esc
Write :wq
Press Enter
```
```
npx hardhat deploy-zksync
  
If you received this answer, then the contract has been deployed:
Greeter was deployed to … 
Contract greets us with Hi there!!
Contract greets us with Hey guys!
```
