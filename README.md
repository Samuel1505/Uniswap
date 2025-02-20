# Swap Exact Tokens for Tokens on Uniswap

## Overview
This script demonstrates how to swap an exact amount of USDC for DAI using Uniswap V2's Router. It impersonates an account with USDC and DAI balances, approves Uniswap to spend tokens, and executes a token swap.

## Requirements
Ensure you have the following dependencies installed:

- [Node.js](https://nodejs.org/)
- [Hardhat](https://hardhat.org/)
- [Ethers.js](https://docs.ethers.org/)
- [@nomicfoundation/hardhat-toolbox](https://www.npmjs.com/package/@nomicfoundation/hardhat-toolbox)

## Setup

1. **Clone the Repository**
   ```sh
   git clone <your-repository-url>
   cd <your-project-folder>
   ```

2. **Install Dependencies**
   ```sh
   npm install hardhat @nomicfoundation/hardhat-toolbox ethers
   ```

3. **Set Up Hardhat** (If not already initialized)
   ```sh
   npx hardhat
   ```
   Select "Create an empty hardhat.config.js" if prompted.

## Script Breakdown
- Defines **USDC** and **DAI** token addresses.
- Uses the **Uniswap Router** contract address.
- Impersonates an account that holds both tokens.
- Approves Uniswap to spend tokens on behalf of the account.
- Executes the `addLiquidity` function on Uniswap.

## Running the Script
1. Ensure your **Hardhat network** is set up to fork the Ethereum mainnet.
   ```sh
   npx hardhat node --fork https://eth-mainnet.alchemyapi.io/v2/YOUR_ALCHEMY_KEY
   ```

2. Run the script:
   ```sh
   npx hardhat run scripts/swapExactTokensForTokens.ts --network hardhat
  
   ```

## Expected Output
- Displays initial USDC and DAI balances of the impersonated account.
- Executes the liquidity addition on Uniswap.
- Displays final balances after the transaction.

## Notes
- The script uses a **Hardhat Impersonation Feature** to interact with an existing Ethereum account.
- Ensure that **your Alchemy or Infura API key** is correctly set up for mainnet forking.
- Change token addresses as needed for different swaps.



