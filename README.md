# My Token
This simple Solidity Program is a Simple Token handling program where you can Mint, Burn, Check your token balance and check your current token supply.

# Description
This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a multiple function that allows the user to Create a token(Mint), Destroy a token(Burn), check your token balance under your address and Checking the current token supply. This program serves as a simple and straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

# Getting Started
**Executing program**
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:
```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // Public variables
    string public TokennName = "JECK";
    string public tokenAbbrv = "JC";
    uint public totalSupply = 0;

    // Mapping variable
    mapping(address => uint) public balances;

    // Mint function
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // Burn function
    function burn(address _address, uint _value) public {
        if (balances[_address] >= _value) {
        totalSupply -= _value;
        balances[_address] -= _value;
    }
}

}
```
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken - Name_Token.sol" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can call the functions of mint, burn, tokenAbbrv, tokenName and totalSupply. First, you need to find your address, to do this find the "account" under "Deploy and run transactions" and then copy the Address. After that, in "Deployed/Unpinned Contracts" section, check out first the "totalSupply" function to know if your token supply is started at 0 value, totalSupply function have the same function to "balance" function but it needs the account address. Next we want to transact some Tokens, you will call the Mint function, under Mint function you need to paste your account address and its value, the value is the ammount of token you want to mint, lets say try to mint atleast 2000 tokens for now. Now we have 1000 tokens, to check this just go to totalSupply or Balance function. Meanwhile the Burn function will deduct token from the address, lets say we want to deduct 1000 tokens from the same address, first paste the address, then in value type 1000, to check if it works call once again the tokenSupply or Balance.

# Author
- NTC PH John Carlo A. Constantino
- @metacraftersio

# Licence
This project is licensed under the MIT License - see the LICENSE.md file for details.
