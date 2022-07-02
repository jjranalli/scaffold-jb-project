# Deploy and test JB-payer contracts with scaffold-eth

This is a simple scaffold-eth which allows to quickly deploy and try out the [extended JB-payer contracts](https://github.com/slice-so/jbpayer-tokens-receiver), compatible with JB V2 projects.

# The contract extension

In addition to the features already provided by the `project payer` contract, which allows JB projects to receive contributions and handle token minting by directly sending ETH to the contract address, **this extension allows JB projects to**:

- Interact with the [Slice protocol](https://slice.so) to easily **split payments and sell anything on decentralized stores**;
- Receive ERC1155 and ERC721 tokens on the project payer address, effectively turning the contract into a NFT vault of the treasury.

# 🏄‍♂️ Quick Start

> checkout the `scaffold-jb` branch

```bash
cd scaffold-jb
git checkout scaffold-jb
```

> install and start your 👷‍ Hardhat chain:

```bash
yarn install
yarn chain
```

> Set up deploy params in the script located in `packages/hardhat/deploy`

> in a second terminal window, 🛰 deploy your contract:

```bash
cd scaffold-nextjs
yarn deploy
```

> in a third terminal window, start your 📱 frontend:

```bash
cd scaffold-nextjs
yarn start
```

🔏 Check smart contract in `JBETHERC20ProjectPayerTokensReceiver.sol` in `packages/hardhat/contracts`

📝 Edit your frontend `index.js` in `packages/react-app/src/pages`

💼 Check deployment scripts in `packages/hardhat/deploy`

📱 Open http://localhost:3000 to see the app

# Notes

- Testing on a local node would require spinning up the JB V2 protocol locally, which is outside the scope of this project. You can test the jb-payer contract by deploying on Rinkeby and interacting with the JB protocol on Rinkeby.
- Head to [this link](https://github.com/slice-so/jbpayer-tokens-receiver) to check out the clone deployments of this contract and other related extensions.
