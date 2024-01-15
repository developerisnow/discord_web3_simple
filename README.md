# Dappcord

# How it works?

## System Architecture: Sequence and Activity Diagrams
![Diagram](https://github.com/developerisnow/real_estate_dapp/blob/main/_docs/img/sequence.png?raw=true)

### Overview
The Dappscord platform integrates blockchain technology to provide a secure and interactive communication space where users must mint NFTs to access different chat channels. This section outlines the sequence of actions and activities that occur from the moment a user connects their wallet to when they can actively participate in a channel.

### Sequence Diagram Explained
The sequence diagram provides a step-by-step visualization of the interactions between the user, their wallet, the Dappscord frontend, the backend server, and the NFT smart contract. It begins with the user connecting their wallet to the system and ends with the user sending and receiving messages in a chat channel.

1. **User Connects Wallet**: The user initiates the process by connecting their digital

wallet to the Dappscord platform.
1. **Authentication**: Upon connecting the wallet, the user is authenticated through their browser, interfacing with the Dappscord website.
2. **Channel Access Request**: The website then communicates with the backend server to request access to a specific chat channel.
3. **NFT Ownership Verification**: The server queries the NFT smart contract to check if the user already owns the NFT granting access to the channel.
4. **NFT Minting Process**:
    - If the user does not own the required NFT, they are prompted to mint one by initiating a transaction, typically involving a transfer of ETH to the NFT contract.
    - After the transaction is confirmed, the NFT is minted, and the user is granted access to the paid channel.
5. Channel Participation: Once access is granted, the user utilizes Socket.io to join the channel and is enabled to read and send messages, engaging with the community.

The sequence diagram is crucial for understanding the interaction order and the role each component plays in facilitating NFT-based access control.
![Diagram](https://github.com/developerisnow/real_estate_dapp/blob/main/_docs/img/activity.png?raw=true)

## Technology Stack & Tools

- Solidity (Writing Smart Contracts & Tests)
- Javascript (React & Testing)
- [Hardhat](https://hardhat.org/) (Development Framework)
- [Ethers.js](https://docs.ethers.io/v5/) (Blockchain Interaction)
- [React.js](https://reactjs.org/) (Frontend Framework)
- [Socket.io](https://socket.io/) (Client & Server communication)

## Requirements For Initial Setup
- Install [NodeJS](https://nodejs.org/en/)

## Setting Up
### 1. Clone/Download the Repository

### 2. Install Dependencies:
`$ npm install`

### 3. Run tests
`$ npx hardhat test`

### 4. Start Hardhat node
`$ npx hardhat node`

### 5. Run deployment script
In a separate terminal execute:
`$ npx hardhat run ./scripts/deploy.js --network localhost`

### 6. Start Socket.io server
`$ node server.js`

### 7. Start frontend
In a separate terminal execute:
`$ npm run start`