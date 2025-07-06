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

#### Deploy Contracts

Edit the deployment script in `deploy/deploy.ts` as needed, then run:

```bash
npx hardhat run deploy/deploy.ts --network <network-name>
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
