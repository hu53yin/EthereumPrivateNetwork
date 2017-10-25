# Ethereum Private Network
Build your Ethereum private-network by step by step instructions

1) Create your Ethereum project folder.
2) Put your genesis.json file into this folder.
3) Create an empty folder it given "chaindata" name.
4) On the shell, go to your project folder and write this command:
  geth --datadir=./chaindata/ init ./genesis.json

5) Start your private-network with this commmand:
  geth --datadir=./chaindata --rpc --rpccorsdomain "http://localhost:8080"

6) And then start your Mist wallet:
  /Applications/Mist.app/Contents/MacOS/Mist --rpc <YourProjectFolderPath>/chaindata/geth.ipc
  
  Example: 
  /Applications/Mist.app/Contents/MacOS/Mist --rpc /Users/huseyingurkan/Documents/Projects/ethereum-private/chaindata/geth.ipc

7) You can also attach to geth:
  geth attach ipc:/<YourProjectFolderPath>/chaindata/geth.ipc
  
  Example: 
  geth attach ipc:/Users/huseyingurkan/Documents/Projects/ethereum-private/chaindata/geth.ipc
