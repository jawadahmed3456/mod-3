# Token Smart Contract 

This repository contains a Solidity smart contract named `Token` that extends the ERC20 token standard and includes additional functionality for managing ownership, minting, burning, and transferring tokens.

## Overview

### ERC20 Token
The `Token` contract is an ERC20-compliant token with the name "token" and symbol "tk." It has a customizable initial supply, and the contract deployer is initially set as the custodian.

### Ownership
The contract includes an ownership mechanism, allowing the custodian to transfer ownership to another address or abandon ownership entirely.

### Token Operations
The contract supports standard ERC20 token operations, including minting, burning, and transferring tokens. Minting tokens is restricted to the custodian.

## Functionality

### 1. Mint Tokens
The custodian can mint additional tokens to a specified beneficiary address using the `minttokens` function. This function is restricted to the custodian.

### 2. Burn Tokens
Token holders can burn their own tokens using the `burnTokens` function, provided they have sufficient funds.

### 3. Transfer Tokens
Token holders can transfer tokens to another address using the `transferTokens` function, ensuring they have enough tokens for the transfer.

### 4. Transfer Ownership
The custodian can transfer ownership of the contract to another address using the `transferOwnership` function. This is useful for transitioning custodianship to another party.

### 5. Abandon Ownership
The custodian can abandon ownership of the contract, setting the custodian address to zero.

## Events

The contract emits two events:
1. `TokensTransferred`: Logs token transfer events, including sender, beneficiary, and the amount transferred.
2. `OwnershipTransferred`: Signals changes in ownership, providing details of the old and new custodians.

## License

This smart contract is licensed under the MIT License. See the provided `LICENSE` file for details.
