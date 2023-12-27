# MyToken Smart Contract

## Overview

The MyToken smart contract is an Ethereum-based ERC-20 token that extends the functionality of the OpenZeppelin ERC20 implementation and incorporates ownership management through the Ownable contract. The token is named "MyToken" with the symbol "MTK."

## Features

### ERC-20 Compliance

MyToken follows the ERC-20 standard, providing standard token functions such as `transfer`, `balanceOf`, and `totalSupply`. This allows for seamless integration with various decentralized applications (DApps) and platforms that support ERC-20 tokens.

### Ownership Management

The token contract is owned by an Ethereum address, which is set during deployment. The ownership functionality is implemented using the Ownable contract from OpenZeppelin, allowing only the owner to perform certain privileged actions.

### Minting

The owner has the exclusive ability to create new tokens by calling the `mint` function. This function requires specifying the recipient's address and the amount (weigh) of tokens to be created. Minting ensures that the total token supply increases, providing a mechanism for token issuance.

### Burning

Token holders can burn their own tokens using the `burn` function. This allows users to reduce their token holdings by specifying the amount (weigh) of tokens they want to burn. The function ensures that the user has a sufficient token balance before executing the burn operation.

### Transfer Function

The standard `transfer` function is overridden to include additional checks for positive token amounts and sufficient token balances. This ensures secure and reliable token transfers between addresses.

### Change Ownership

The current owner can transfer ownership to another address using the `setOwner` function. This is a secure way to change control of the token contract while ensuring that the new owner address is valid.

## Usage

To deploy the MyToken contract, deployers can use the specified SPDX-License-Identifier and Solidity version. After deployment, the owner can mint new tokens, transfer ownership, and manage the token contract.

## License

This smart contract is released under the MIT License. See the provided SPDX-License-Identifier for details.
