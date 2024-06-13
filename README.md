In the assessment, there is a need to create a smart contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply).
There will be a mapping of addresses to balances (address => uint).
You will have a mint function that takes two parameters: an address and a value. The function will then increase the total supply by that number and increase the balance of the address by that amount.
Your contract will have a burn function that operates in opposition to the mint function. It will take an address and value and then deduct the value from the total supply and from the balance of the address.
Lastly, your burn function should have conditionals to ensure that the balance of the account is greater than or equal to the amount that is supposed to be burned.

![image](https://github.com/ShaynaSingh/Assessment-Solidity/assets/137195755/220fd850-9a56-40da-a779-3dca2af31c11)
This is a way of fullfilling the requirements of the project.
