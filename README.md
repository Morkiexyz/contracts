# Morkie Platform Contracts

Morkie is a web3 application leveraging Thirdweb integration to facilitate seamless blockchain-based interactions through smart contracts. Our platform is meticulously designed with a focus on performance and user experience. As proud participants in the Thirdweb Startup Program, we build on the robust infrastructure provided by Thirdweb, utilizing their suite of advanced smart contracts.

## Smart Contracts

Our project utilizes the following smart contracts from Thirdweb:

- **OpenEditionERC721**: [Version 5.0.1](https://thirdweb.com/thirdweb.eth/OpenEditionERC721/5.0.1) - This contract allows for the creation and management of open edition NFTs, enabling users to mint and trade digital assets securely.

- **StakeERC20**: [Version 5.0.1](https://thirdweb.com/thirdweb.eth/TokenStake) - This contract allows users to stake their ERC-20 tokens and receive ERC-20 tokens as staking rewards (different from the staked tokens).

- **StakeERC721**: [Version 5.0.1](https://thirdweb.com/thirdweb.eth/NFTStake) - This contract allows users to stake their ERC-721 NFTs and receive ERC-20 tokens as staking rewards.

- **Token**: [Version 5.0.1](https://thirdweb.com/thirdweb.eth/TokenERC20) - The Token contract is suited for creating a digital currency and is compliant with the ERC20 standard.

- **Managed Account Factory**: [Version 1.57.27](https://thirdweb.com/thirdweb.eth/ManagedAccountFactory) - This contract allows to deploy upgradeable smart wallets for users, with the ability to push updates to all users


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

