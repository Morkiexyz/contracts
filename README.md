import { Web3Button } from "@thirdweb-dev/react";

# Morkie Platform Contracts

Morkie is a web3 application leveraging [Thirdweb](https://thirdweb.com/) integration to facilitate seamless blockchain-based interactions through smart contracts. Our platform is meticulously designed with a focus on performance and user experience. As proud participants in the Thirdweb Startup Program, we build on the robust infrastructure provided by [Thirdweb](https://thirdweb.com/), utilizing their suite of advanced pre-built smart contracts.

## Table of Contents

1. [Smart Contracts](#smart-contracts)
2. [Installation](#installation)
3. [Usage](#usage)
4. [Example: How We Call the Smart Contract](#example-how-we-call-the-smart-contract)
5. [Testing](#testing)
6. [Contributing](#contributing)
7. [License](#license)
8. [Contact](#contact)

## Smart Contracts

Our project utilizes the following smart contracts from [Thirdweb](https://thirdweb.com/):

- **OpenEditionERC721**: [Version 5.0.1](https://thirdweb.com/thirdweb.eth/OpenEditionERC721/5.0.1) - This contract allows for the creation and management of open edition NFTs, enabling users to mint and trade digital assets securely.

- **StakeERC20**: [Version 5.0.1](https://thirdweb.com/thirdweb.eth/TokenStake) - This contract allows users to stake their ERC-20 tokens and receive ERC-20 tokens as staking rewards (different from the staked tokens).

- **StakeERC721**: [Version 5.0.1](https://thirdweb.com/thirdweb.eth/NFTStake) - This contract allows users to stake their ERC-721 NFTs and receive ERC-20 tokens as staking rewards.

- **Token**: [Version 5.0.1](https://thirdweb.com/thirdweb.eth/TokenERC20) - The Token contract is suited for creating a digital currency and is compliant with the ERC20 standard.

- **Managed Account Factory**: [Version 1.57.27](https://thirdweb.com/thirdweb.eth/ManagedAccountFactory) - This contract allows deploying upgradeable smart wallets for users, with the ability to push updates to all users.

All the contracts are available in the [Thirdweb GitHub repository](https://github.com/thirdweb-dev/contracts).

## Installation

To get started with Morkie, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/morkie.git
    cd morkie
    ```

2. Create a `.env` file and add your environment variables:
    ```
    REACT_APP_API_URL=https://your-api-url
    REACT_APP_THIRDWEB_API_KEY=your-thirdweb-api-key
    ```

3. Start the development server:
    ```bash
    npm start
    ```

## Usage

To use the Morkie platform, you need to interact with the smart contracts deployed on the blockchain. The following example demonstrates how to call a smart contract using the `Web3Button` component.

## Example: How We Call the Smart Contract

```jsx
<Web3Button
  contractAddress="0x5A3B5f1B364eF597e3E6E994810ae5f3918C7D65"
  action={async (contract) => {
    await contract.erc721.claim(value);
  }}
  onSuccess={(result) => alert("Success!")}
>
  Mint
</Web3Button>
