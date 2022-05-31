# You Me and Solidity

![Logo](https://i.ibb.co/VLTK5Gq/solidity-nedir-removebg-preview.png)

## Remix IDE
You can start writting solidity contracts directly on `https://remix.ethereum.org/`
(In the contracts file of remix IDE, there are some demo solidity contracts. You can give it a look to these codes. But don't worry if you don't understand anything. We are going to learn everything to write codes like these and beyond. 

## SPDX License Identifier
The Solidity compiler encourages to use machine-readable SPDX license identifiers at the top of the contract, mainly for licensing, copyright issues.

`// SPDX-License-Identifier: MIT`

There many licence identifieres. [more](https://spdx.org/licenses/)


## Contract Compilation
Basically smart contracts compiled into 2 parts. ABI and Byte Code

![Logo](https://i.ibb.co/zszQzTF/Contract-source-code.png)

### ABI: 
Simply Application Binary Interface (ABI) manages connecting to that specific smart contract, handle function calls, data type, data transfer from that contract. 
Markup : <details>
           <summary>ABI Example</summary>
           <p>[
                {
                    "inputs": [
                        {
                            "internalType": "uint256",
                            "name": "num",
                            "type": "uint256"
                        }
                    ],
                        "name": "store",
                        "outputs": [],
                        "stateMutability": "nonpayable",
                        "type": "function"
                    }
                ]
            </p>
         </details>

### Byte Code: 
Byte code is public, readable and immutable code that is deployed to the smart contract. Then the byte code is converted to low level opcode and EVM executes the opcode.
Markup : <details>
           <summary>Byte Code Example</summary>
           <p>
            {
                "functionDebugData": {},
                "generatedSources": [],
                "linkReferences": {},
                "object": "608060405234801561001057600080fd5b5060e38061001f6000396000f3fe6080604052348015600f57600080fd5b506004361060285760003560e01c80636057361d14602d575b600080fd5b60436004803603810190603f91906062565b6045565b005b8060008190555050565b600081359050605c816099565b92915050565b60006020828403121560755760746094565b5b6000608184828501604f565b91505092915050565b6000819050919050565b600080fd5b60a081608a565b811460aa57600080fd5b5056fea2646970667358221220fb1ba4f87b23320a7a466e010a2625cb6a8e38166b3efa45d143d21447116a4664736f6c63430008070033",
                "opcodes": "PUSH1 0x80 PUSH1 0x40 MSTORE CALLVALUE DUP1 ISZERO PUSH2 0x10 JUMPI PUSH1 0x0 DUP1 REVERT JUMPDEST POP PUSH1 0xE3 DUP1 PUSH2 0x1F PUSH1 0x0 CODECOPY PUSH1 0x0 RETURN INVALID PUSH1 0x80 PUSH1 0x40 MSTORE CALLVALUE DUP1 ISZERO PUSH1 0xF JUMPI PUSH1 0x0 DUP1 REVERT JUMPDEST POP PUSH1 0x4 CALLDATASIZE LT PUSH1 0x28 JUMPI PUSH1 0x0 CALLDATALOAD PUSH1 0xE0 SHR DUP1 PUSH4 0x6057361D EQ PUSH1 0x2D JUMPI JUMPDEST PUSH1 0x0 DUP1 REVERT JUMPDEST PUSH1 0x43 PUSH1 0x4 DUP1 CALLDATASIZE SUB DUP2 ADD SWAP1 PUSH1 0x3F SWAP2 SWAP1 PUSH1 0x62 JUMP JUMPDEST PUSH1 0x45 JUMP JUMPDEST STOP JUMPDEST DUP1 PUSH1 0x0 DUP2 SWAP1 SSTORE POP POP JUMP JUMPDEST PUSH1 0x0 DUP2 CALLDATALOAD SWAP1 POP PUSH1 0x5C DUP2 PUSH1 0x99 JUMP JUMPDEST SWAP3 SWAP2 POP POP JUMP JUMPDEST PUSH1 0x0 PUSH1 0x20 DUP3 DUP5 SUB SLT ISZERO PUSH1 0x75 JUMPI PUSH1 0x74 PUSH1 0x94 JUMP JUMPDEST JUMPDEST PUSH1 0x0 PUSH1 0x81 DUP5 DUP3 DUP6 ADD PUSH1 0x4F JUMP JUMPDEST SWAP2 POP POP SWAP3 SWAP2 POP POP JUMP JUMPDEST PUSH1 0x0 DUP2 SWAP1 POP SWAP2 SWAP1 POP JUMP JUMPDEST PUSH1 0x0 DUP1 REVERT JUMPDEST PUSH1 0xA0 DUP2 PUSH1 0x8A JUMP JUMPDEST DUP2 EQ PUSH1 0xAA JUMPI PUSH1 0x0 DUP1 REVERT JUMPDEST POP JUMP INVALID LOG2 PUSH5 0x6970667358 0x22 SLT KECCAK256 0xFB SHL LOG4 0xF8 PUSH28 0x23320A7A466E010A2625CB6A8E38166B3EFA45D143D21447116A4664 PUSH20 0x6F6C634300080700330000000000000000000000 ",
                "sourceMap": "71:112:0:-:0;;;;;;;;;;;;;;;;;;;"
            }
           </p>
         </details>

![Logo](https://i.ibb.co/3hpgssb/et5PNG.png)

### EVM: 
EVM is a software version of CPU that executes the compiled opcode of solidity smart contracts. EVM keeps track of the current state of the blockchain. Whenever a smart contract or Transaction happens, EVM runs the opcode in all the nodes and changes the state of the blockchain. 