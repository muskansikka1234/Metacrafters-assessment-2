# Project Title

Token contract with mint and burn functionality.

## Description

This project involves the creation of a smart contract on the Ethereum blockchain that defines a custom cryptocurrency token. The key features and functionalities of this contract include:
1. Public token details
Token Name: A publicly accessible string that holds the name of the token.
Token Abbreviation (Abbrv.): A publicly accessible string that holds the token's abbreviation (e.g., QTC for Quantum Coin).
Total Supply: A publicly accessible unsigned integer that holds the total number of tokens in circulation.

2. Address to balance mapping
   The contract maintains a mapping (address => uint) that tracks the balance of each address holding the token. This ensures that the balance of tokens for any address can be queried and managed effectively.

3. Mint Function:
Functionality: Allows the creation of new tokens.

4. Burn Function:
Functionality: Allows the destruction of existing tokens.

## Getting Started

### Executing program


```
Pragma solidity ^0.8.3;
contract MyToken {

    // public variables here
    string public tokenName = "Quantum Coin";
    string public tokenAbbrv = "QTC";
    uint public TotalSupply = 0;

    // mapping variable here
    mapping(address => uint)public balances;

    // mint function
    function mint(address _address, uint _value) public {
        TotalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value) public {
        if(balances[_address] >= _value) {
            TotalSupply -= _value;
        balances[_address] -= _value;

        }
        
    }

}

```

## Help

1. Ensure that the Solidity version specified in your contract (pragma solidity ^0.8.0;) matches the version of the Solidity compiler.
2. Double-check the syntax of your Solidity code. Missing semicolons, incorrect variable declarations, or misplaced brackets can cause compilation errors.

## Authors

Contributors names and contact info

Muskan Sikka  
muskansikka1234@gmail.com


## License

This project is licensed under the [SPDX-License-Identifier: MIT] License.
