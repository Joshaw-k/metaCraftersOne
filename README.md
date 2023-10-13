# MyToken Contract

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain.
This contract has public variables that store the details about my token (tokenName, tokenAbbrv, totalSupply).
This contract has a mapping of addresses to balances.
This has a mint function that takes two parameters that increases the total supply by the value specified to mint and increases the balance of the address that will be minted by that value.
This contract has a burn function, which works the opposite of the mint function, as it will destroy tokens.
It will then deduct the value specified to burn from the total supply and from the balance of the address that a value will be burned from.
Lastly, the burn function has a condition to make sure the balance of account is greater than or equal to the amount that is supposed to be burned.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity 0.8.19;

contract MyToken {
    // public variables here
    string public tokenName = "MYTOKEN";
    string public tokenAbbrv = "MTN";
    uint256 public totalSupply = 0;

    // mapping variable here
    mapping(address => uint256) public balances;

    // mint function
    function mint(address to, uint256 value) public {
        totalSupply += value;
        balances[to] += value;
    }

    // burn function
    function burn(address from, uint256 value) public {
        if (balances[to] >= value) {
            totalSupply -= value;
            balances[to] -= value;
        }
    }
}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.19" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint function. Click on the "MyToken" contract in the left-hand sidebar, and then fill in the input tab beside the mint function with the address you want to mint to and the amount you want to mint. When you are done,click on the "mint" function. Check that the balance of the address you minted to has been incremented by the amount you minted and that the total supply has also been incremented by that same about. If you want to call the burn function you can fill in the input tab beside the burn function with the address you want to burn from and the amount you want to burn. Check that the balance of the address you burned from has been decremented by the amount you burnt and that the total supply has also been decremented by that same about.

## Authors

Joshaw-k  
[Koniesjay](https://twitter.com/awinrin21)

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
