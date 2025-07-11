# FHEVM Hardhat Template

This project provides a ready-to-use Hardhat template for developing, testing, and deploying Solidity smart contracts that leverage Fully Homomorphic Encryption (FHE) on the FHEVM protocol.

## Features

- **FHE-Enabled Smart Contracts**: Write and deploy Solidity contracts that use FHE for privacy-preserving computations.
- **Pre-configured Hardhat Environment**: Includes all necessary dependencies and configuration for FHEVM development.
- **Sample Contracts**: Example contracts (`FHECounter.sol`, `Counter.sol`) to help you get started quickly.
- **Automated Testing**: Sample test scripts using Hardhat and ethers.js.
- **Deployment Scripts**: Ready-to-use deployment scripts for your contracts.
- **Task Scripts**: Custom Hardhat tasks for interacting with your contracts.

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v16 or later recommended)
- [Yarn](https://yarnpkg.com/) or [npm](https://www.npmjs.com/)
- [Hardhat](https://hardhat.org/)

> **Note:** Hardhat does not support odd-numbered Node.js versions. If you're using one (e.g., v21.x, v23.x), Hardhat will display a persistent warning message and may behave unexpectedly.

### Installation

1. Clone this repository:
   ```bash
   git clone <your-repo-url>
   cd <project-directory>
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn install
   ```

### Usage

#### Compile Contracts

```bash
npx hardhat compile
```

#### Run Tests

```bash
npx hardhat test
```

## Testing and Interacting on Sepolia Testnet

You can test your FHEVM smart contract using real encrypted values by running your tests and deploying on the Sepolia Testnet.

### 1. Rebuild the Project for Sepolia

From the root project directory:

```bash
npx hardhat compile --network sepolia
```

### 2. Deploy the FHECounter Smart Contract on Sepolia

```bash
npx hardhat deploy --network sepolia
```

### 3. Check the Deployed FHECounter Contract FHEVM Configuration

From the root project directory:

```bash
npx hardhat fhevm check-fhevm-compatibility --network sepolia --address <deployed contract address>
```

> If an internal exception is raised, it likely means the contract was not properly compiled for the Sepolia network.

### 4. Interact with the Deployed FHECounter Contract

From the root project directory:

#### Decrypt the Current Counter Value

```bash
npx hardhat --network sepolia task:decrypt-count
```

#### Increment the Counter by 1

```bash
npx hardhat --network sepolia task:increment --value 1
```

#### Decrypt the New Counter Value

```bash
npx hardhat --network sepolia task:decrypt-count
```

#### Run Custom Tasks

List available tasks:

```bash
npx hardhat help
```

Run a specific task (e.g., accounts):

```bash
npx hardhat accounts
```

## Documentation

- [FHEVM Documentation](https://docs.zama.ai/fhevm)
- [FHEVM Hardhat Quick Start Tutorial](https://docs.zama.ai/protocol/solidity-guides/getting-started/quick-start-tutorial)
- [Setup Guide](https://docs.zama.ai/protocol/solidity-guides/getting-started/setup)
- [Writing and Running Tests](https://docs.zama.ai/protocol/solidity-guides/development-guide/hardhat/write_test)
- [FHEVM Hardhat Plugin](https://docs.zama.ai/protocol/solidity-guides/development-guide/hardhat)

## License

This project is licensed under the MIT License.
