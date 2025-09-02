# DNG Coin (DNG)

An ERC-20 token deployed on **Sepolia Testnet** as part of my Web3 learning and portfolio showcase.  

- **Name:** DNG Coin  
- **Symbol:** DNG  
- **Decimals:** 18  
- **Total Supply:** 1,000,000 DNG  
- **Network:** Ethereum Sepolia Testnet  
- **Contract Address:** [0xb6338a9812c325fc42552dabc72b45cbb30b5b29](https://sepolia.etherscan.io/address/0xb6338a9812c325fc42552dabc72b45cbb30b5b29)


---

## 📄 Smart Contract
Source code (Solidity 0.8.20):

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract DNGCoin is ERC20 {
    constructor(uint256 initialSupply) ERC20("DNG Coin", "DNG") {
        _mint(msg.sender, initialSupply * 10 ** decimals());
    }
}
