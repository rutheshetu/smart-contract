Smart Contracts: A Blockchain Program
A smart contract is blockchain-deployed code. For example:
contract Agreement { address recipient; bool conditionIsMet; function payout() external { if(conditionIsMet) { sendValue(recipient); } } // ... }
Deploying a Contract
⚙️ compile your solidity to bytecode
✉️ send a transaction containing the bytecode to an EVM node
🏡 the node calculates an address for your new contract
Contract Deployment
  (https://github.com/AstuCSE-BC/solidity-group-project/blob/main/Eyob-Mulugeta/0-smart-contracts/imgs/contract-deployment.png)
OpcodeNameDescriptionGas0x00STOPHalts execution00x01ADDAddition operation30x02MULMultiplication operation50x03SUBSubtraction operation3
https://ethereum.org/en/developers/docs/evm/opcodes/
Key Takeaways
⚙️ Contracts are compiled to creation bytecode
⛓️ The data field contains your creation bytecode
📭 The to field is left blank to deploy a contract
🏡 Your contract will have an address, balance and runtime bytecode
Transaction Life Cycle
  (https://github.com/AstuCSE-BC/solidity-group-project/blob/main/Eyob-Mulugeta/0-smart-contracts/imgs/contract-communication.png)
Key Takeaways
🥾 Transactions begin at an EOA
☝️ Transactions occur sequentially
⛽️ Transactions set a gas limit
🎯 Transactions send calldata, targetting a contract method
🌐 Similarly smart contracts can call each other within the one transaction
