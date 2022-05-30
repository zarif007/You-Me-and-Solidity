# You Me and Solidity

![Logo](https://i.ibb.co/VLTK5Gq/solidity-nedir-removebg-preview.png)

## Remix IDE
You can start writting solidity contracts directly on `https://remix.ethereum.org/`
(In the contracts file of remix IDE, there are some demo solidity contracts. You can give it a look to these codes. But don't worry if you don't understand anything. We are going to learn everything to write codes like these and beyond. 

## SPDX License Identifier
The Solidity compiler encourages to use machine-readable SPDX license identifiers at the top of the contract, mainly for licensing, copyright issues.

`// SPDX-License-Identifier: MIT`

There many licence identifier. [For more](https://spdx.org/licenses/)


## Contract Compilation
Basically smart contracts compiled into 2 parts.

![Logo](https://i.ibb.co/zszQzTF/Contract-source-code.png)

### ABI: 
Simply Application Binary Interface (ABI) manages connecting to that specific smart contract, handle function calls, data type, data transfer from that contract. 

### Byte Code: 
Byte code is public, readable and immutable code that is deployed to the smart contract. Then the byte code converts to low level opcode and EVM executes the opcode.

![Logo](https://i.ibb.co/3hpgssb/et5PNG.png)

### EVM: 
EVM is a software version of CPU that executes the compiled opcode of solidity smart contracts. EVM keeps track of the current state of the blockchain. Whenever a smart contract or Transaction happens, EVM runs the opcode in all the nodes and changes the state of the blockchain. 