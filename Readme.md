CREATING A TOKEN!
Creating our own token

Description
Introduction to Data Types
Mapping in Solidity
Functions Demonstration
Getting Started
Installing
• You can use the online Ethereum IDE

Executing program
• Go to Ethereum IDE(https://remix.ethereum.org/)
• Create a new file and write your code • // SPDX-License-Identifier: MIT • pragma solidity 0.8.25;

• contract MyToken { • • // public variables here • string public tokenName = "META"; • string public tokenAbbrv = "MTA"; • uint public totalSupply = 0; • • // mapping variable here • mapping(address => uint) public balances; • • // mint function • function mint (address _address, uint _value) public { • totalSupply += _value; • balances[_address] += _value; • } •
• // burn function • function burn (address _address, uint _value) public { • if (balances[_address] >= _value) { • totalSupply -= _value; • balances[_address] -= _value; • } • } •
• } •

• Then complie the code using solidity compiler of IDE Remember the auto compiler option should be enabled

• Then go to Deploy and Run transactions

Click on deploy
Something like this will come in the terminal 2. Copy account and paste in the mint function address parameter and pass 1000 as value in the value parameter 3. Then check the total supply

Now paste the same address in the burn function and pass let say value 500 in the value parameter
Then again check the total supply
