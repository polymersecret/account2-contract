## Team Members

- @morrisernest - Developer


## Introduction

Our project aims to build a L2 native token bridge. We plan to build standardized vault for locking tokens and minting tokens.


## Steps to reproduce
1. Contract dependens install, compile and deploy
```
just install
npx hardhat compile
just deploy optimism base
```
2. Copy the result of contract deployed(port address) or go to /config/config.json copy sendUniversalPacket.optimism.portAddr and sendUniversalPacket.base.portAddr
3. Go to /ibc-token-bridge/src/App.vue replace `OP_PORT_ADDRESS` and `BASE_PORT_ADDRESS` with port address from step 2
4. Go to /artifacts/contracts/PolymerBridge.sol/PolymerBridge.json file to copy ABI
5. Go to /ibc-token-bridge/src/abi.js replace `CONTRACT_ABI` with ABI from setp 4
6. clone frontend project
```
npm i
npm run serve
```


## Proof of testnet interaction

After following the steps above you should have interacted with the testnet. You can check this at the [IBC Explorer](https://explorer.ethdenver.testnet.polymer.zone/).

Here's the data of our application:

- Contract (OP Sepolia) : 0xB49a654EcED1CF6FabE4C347faD2089490889fCE
- Contract (Base Sepolia): 0xB49a654EcED1CF6FabE4C347faD2089490889fCE
- Channel (OP Sepolia): 0xB49a654EcED1CF6FabE4C347faD2089490889fCE
- Channel (Base Sepolia): 0xB49a654EcED1CF6FabE4C347faD2089490889fCE

- Proof of Testnet interaction:
    - [SendTx](https://optimism-sepolia.blockscout.com/tx/0xc6c487902b7823d7f5ca3091c989b81bcccfcb4d3766825bcd7e84ab75eb2ea8)
    - [RecvTx](https://base-sepolia.blockscout.com/tx/0xdd978624d563d32b9a009e6d0de124c90ed3f466970568399d2b68f812269eeb)
    - [Ack](https://base-sepolia.blockscout.com/tx/0xdd978624d563d32b9a009e6d0de124c90ed3f466970568399d2b68f812269eeb)

## What we learned

We learned how to build a l2 bridge using polymer

## Future Improvements
Maybe we maintain the security of the vault, such as multi-signature
Support more L2 

## License
Apache 2.0