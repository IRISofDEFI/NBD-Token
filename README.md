# NBDToken - ERC20 Token

## Overview

`NBDToken` is a simple ERC-20 compliant token implemented using OpenZeppelin's well-audited ERC20 standard. This contract is suitable for educational purposes, basic token deployment, and prototype development on the Ethereum blockchain.

The contract mints a fixed initial supply of **1,000 tokens** (with 18 decimals) to the deployer's address upon deployment.

---

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Contract Explanation](#contract-explanation)
- [Deployment](#deployment)
- [Usage](#usage)
- [Security Considerations](#security-considerations)
- [License](#license)

---

## Features

- ✅ Fully ERC20-compliant
- ✅ Built on OpenZeppelin standards
- ✅ Mints 1000 tokens to deployer upon deployment
- ✅ Supports 18 decimal places

---

## Technologies Used

- Solidity ^0.8.0
- OpenZeppelin Contracts (ERC20 standard)
- Ethereum-compatible networks (Sepolia, Goerli, Mainnet, etc.)

---

## Contract Explanation

```solidity
pragma solidity ^0.8.0;

import "https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/ERC20.sol";

contract NBDToken is ERC20 {
    constructor(string memory _name, string memory _symbol) ERC20(_name, _symbol) {
        _mint(msg.sender, 1000 * 10 ** 18);
    }
}
## NBD Contract Address: 0x301D07422e5a70F7Ee1801977c8452103D2FCe59

## 🔍 Components
import ... ERC20.sol
This imports OpenZeppelin’s secure and standardized implementation of the ERC20 token interface.

It includes all the core functionality like transfers, balances, approvals, and events.

contract NBDToken is ERC20
Inherits from OpenZeppelin’s ERC20, gaining full ERC20 functionality.

constructor(string memory _name, string memory _symbol)
Accepts the token’s name and symbol as parameters (e.g., "New Blockchain Dollar" and "NBD").

Calls the parent constructor to initialize these values.

_mint(msg.sender, 1000 * 10 ** 18);
Mints 1,000 tokens (represented as 1000 * 10^18 because ERC20 tokens use 18 decimals by default).

Sends the initial supply to the address deploying the contract.

Deployment
Using Remix
Open Remix IDE

Create a new file NBDToken.sol and paste the contract code.

Compile the contract with Solidity compiler 0.8.x

Deploy:

Provide name (e.g., "New Blockchain Dollar")

Provide symbol (e.g., "NBD")

Choose an environment (e.g., Injected Web3 for MetaMask)

Usage
Example Token Info (after deploying with "New Blockchain Dollar" and "NBD"):
Property	Value
Name	New Blockchain Dollar
Symbol	NBD
Decimals	18
Total Supply	1,000 NBD

Basic Interactions (via Web3 tools like Ethers.js or Web3.js):
balanceOf(address) → Check balance of an address.

transfer(address to, uint256 amount) → Transfer tokens.

approve(address spender, uint256 amount) → Approve another address to spend.

transferFrom(address from, address to, uint256 amount) → Transfer on behalf of someone else (after approval).

Security Considerations
This is a basic token contract and does not include advanced features like pausable transfers, mint/burn permissions, or role-based access.

Not recommended for production without further audits and access control features.

License
This project is licensed under the MIT License.

---

Let me know if you'd like a version that includes logo badges, deployment scripts, test instructions, or hardcoded token values (i.e., fixed name and symbol instead of parameters).

