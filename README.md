# TomyToken Smart Contract

The `TomyToken` is an ERC20 token smart contract deployed on the Ethereum blockchain. It facilitates the creation, management, and manipulation of a fungible token named "Tonmay" with the symbol "TOMY". This contract includes features for minting, burning, transferring tokens, and checking balances.

## Description

The `TomyToken` contract adheres to the ERC20 standard, a widely accepted protocol for fungible tokens on Ethereum. Key functionalities of the contract include:

- **Minting**: Allows the contract owner to mint new tokens.
- **Burning**: Permits any token holder to burn their tokens.
- **Balance Checking**: Token holders can check their own balance.
- **Token Transfer**: Token holders can transfer tokens to other addresses.
- **Total Supply**: Provides the total supply of the tokens.

## Getting Started

### Executing the Contract

To deploy and interact with the `TomyToken` smart contract, follow these steps using Remix, an online Solidity IDE:

1. **Open Remix:**
   - Navigate to [Remix IDE](https://remix.ethereum.org/).

2. **Create a New File:**
   - Click the "+" icon in the left-hand sidebar.
   - Save the new file with a `.sol` extension (e.g., `TomyToken.sol`).

3. **Add the Code:**
   - Copy and paste the following Solidity code into your file:

    ```solidity
    pragma solidity ^0.8.4;

    import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
    import "@openzeppelin/contracts/access/Ownable.sol";

    contract TomyToken is ERC20, Ownable {
        constructor(uint256 initialSupply) ERC20("Tonmay", "TOMY") {
            _mint(msg.sender, initialSupply);
        }
   ...
    ```

4. **Compile the Code:**
   - Go to the "Solidity Compiler" tab in the left-hand sidebar.
   - Set the "Compiler" option to "0.8.4" or another compatible version.
   - Click the "Compile TomyToken.sol" button.

5. **Deploy the Contract:**
   - Go to the "Deploy & Run Transactions" tab in the left-hand sidebar.
   - Select "TomyToken" from the contract dropdown menu.
   - Provide an initial supply value and click the "Deploy" button.

6. **Interact with the Contract:**
   - Use the deployed contract to:
     - **Mint Tokens**: `mintTokens(address to, uint256 amount)`
     - **Burn Tokens**: `burnTokens(uint256 amount)`
     - **Check Balance**: `myBalance()`
     - **Transfer Tokens**: `transferTokens(address to, uint256 amount)`
     - **Check Total Supply**: `totalSupply()`

## Authors

Metacrafter Chris  
Tonmay

## OverView

![Token Overview](https://github.com/user-attachments/assets/93d54ed4-facd-446e-ac36-9ba798228d7f)
