# Token Creation - Smart Contract

This Solidity program is a simple "Token Creation" program that demonstrates the basic syntax and functionality of the Solidity programming language. 

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract will have public variables that store the details about the coin (Token Name, Token Abbrv., Total Supply).
There will be a mapping of addresses to balances (address => uint).
We need to create a mint function that takes two parameters: an address and a value. The function will then increase the total supply by that number and increase the balance of the address by that amount.
The contract will also have a burn function that operates in opposition to the mint function. It will take an address and value and then deduct the value from the total supply and from the balance of the address.
Lastly, the burn function should have conditionals to ensure that the balance of the account is greater than or equal to the amount that is supposed to be burned.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., myToken.sol). Copy and paste the following code into the file which works as a structure for the smart contract.

```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

/*
       REQUIREMENTS
    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    2. Your contract will have a mapping of addresses to balances (address => uint)
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount
    4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
    5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.
*/

contract MyToken {

    // public variables here

    // mapping variable here

    // mint function

    // burn function

}
```
The public variables I have used are :
```
    string public tokenName = "CRAFT";
    string public tokenAbbrv = "CRT";
    uint   public totalSupply = 0;
```
The mint function can be written as:
```
function mint (address _address, uint _val) public {
      totalSupply += _val;
      balances[_address] += _val;
    }
```
Similarly, the burn function can be written as :
```
 function burn (address _address, uint _val) public {
      if (balances[_address] >= _val) {
        totalSupply -= _val;
        balances[_address] -= _val;
      }
    }
```
fulfilling the requirements for the burn function as well as the use of conditional statements.

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" , and then click on the "Compile myToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "myToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by providing "address" and "value" to the mint and burn function and clicking the "transact" button. 

## Authors

Shayna Singh 


