# Degen Token

Degen Token is an ERC-20 token smart contract deployed on the Avalanche network. It provides the functionality to mint new tokens, transfer tokens between addresses, approve spenders, transfer tokens on behalf of the sender, burn tokens, and check token balances.

## Contract Details

**Name**: Degen Token
**Symbol**: DEGEN
**Decimals**: 18
**Total Supply**: 0 (initially)
**Owner**: Contract deployer

## Contract Functions

### mint

```solidity
function mint(address to, uint256 amount) public onlyOwner
```

The `mint` function allows the contract owner to create new tokens and distribute them to players as rewards. The owner can specify the recipient's address (`to`) and the amount of tokens to be minted (`amount`). Only the contract owner can call this function.

### transfer

```solidity
function transfer(address to, uint256 amount) public returns (bool)
```

The `transfer` function allows token holders to transfer their tokens to other addresses. The sender specifies the recipient's address (`to`) and the amount of tokens to be transferred (`amount`). The function checks if the recipient address is valid, the amount is greater than zero, and the sender has sufficient balance. If the conditions are met, the transfer is executed.

### approve

```solidity
function approve(address spender, uint256 amount) public returns (bool)
```

The `approve` function allows a token holder to approve a spender to spend tokens on their behalf. The token holder specifies the spender's address (`spender`) and the amount of tokens to be approved (`amount`). The function checks if the spender address is valid. If so, it sets the spender's allowance to the approved amount.

### transferFrom

```solidity
function transferFrom(address from, address to, uint256 amount) public returns (bool)
```

The `transferFrom` function allows the approved spender to transfer tokens from one address to another on behalf of the sender. The sender specifies their address (`from`), the recipient's address (`to`), and the amount of tokens to be transferred (`amount`). The function checks if the sender and recipient addresses are valid, the amount is greater than zero, and both the sender has sufficient balance and the spender has sufficient allowance. If the conditions are met, the transfer is executed.

### burn

```solidity
function burn(uint256 amount) public returns (bool)
```

The `burn` function allows any token holder to burn their tokens, removing them from circulation. The token holder specifies the amount of tokens to be burned (`amount`). The function checks if the amount is greater than zero and the sender has sufficient balance. If the conditions are met, the tokens are burned by reducing the total supply and deducting the tokens from the sender's balance.

## License

This code is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.
SPDX-License-Identifier: MIT

Contact - adi62333@gmail.com for future refrences
