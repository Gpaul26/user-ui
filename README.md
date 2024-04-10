# Lottery gamification using Polymer IBC

## Idea

The idea centers on creating a decentralized application (dApp) on a blockchain platform, with the goal of improving user engagement and interaction with the Polymer Labs IBC App through gamification. The primary function of this dApp includes a recurring bridge challenge that takes place every 2 hours. During each interval, the dApp specifies a particular direction that participants must fulfill by sending a package using a universal channel—a technology that facilitates package transfer across various blockchain platforms.

## Usage

1. Running the Front-end

- You just need to run it 
```bash
npm install && 
npm start
```
- You site at: http://localhost:3000/ 

2. For Back-end, You clone the project at [here](https://github.com/bridge-lottery/lottery-service)

- Set up and run it by: 
```bash
npm install && 
nodemon app.js
```

3. For Contract, you clone the project at [here](https://github.com/bridge-lottery/ibc-app-solidity-template). In this repo, following the readme to install and temperarilly deploy contracts and send packets.

## Key Feature

### Scheduled Challenges:

The dApp will announce challenges every 2 hours. Each challenge entails a specific task that users must complete using a universal channel, such as transferring a package from one blockchain to another according to the dApp's instructions.

### Participation Monitoring:

The dApp tracks and logs participants' actions to verify adherence to the challenge requirements. This includes confirming completion of bridge transactions within the stipulated time frame.

### Performance Compilation:

Following four consecutive challenges (spanning an 8-hour period, with four announcements), the dApp compiles performance data from all participants. It evaluates their speed and accuracy in executing bridge transactions as specified in the challenges.

### Reward Allocation:

The top 10 participants demonstrating the fastest and most accurate execution of bridge transactions across the four challenges receive rewards.

The reward system is integrated into the dApp, utilizing smart contracts to automatically distribute prizes based on participants' rankings.

Rankings are determined by users' transaction speed.

The formula used is as follows:

```
Gap = Sent_Time - Announcement_Time
Total = Gap1 + Gap2 + Gap3 + Gap4
```

The participant with the shortest total time wins!

## Technical Considerations

### Smart Contract Development:

The foundation of the dApp involves developing secure and efficient smart contracts responsible for managing challenge announcements, tracking user participation, aggregating performance data, and facilitating rewards distribution.

### Blockchain Infrastructure:

The dApp utilizes the Polymer IBC.

### User Interface (UI) and Experience (UX):

An intuitive interface is essential for engaging participants. The dApp should offer clear instructions for each challenge, display real-time rankings, and provide a seamless experience for tracking challenge progress and rewards.

### Security Measures:

Given the financial stakes involved and the utilization of blockchain bridges, the dApp must implement robust security measures to prevent fraud, maintain transaction integrity, and safeguard user interests.


## Proof of testnet interaction
- [sendTx](https://optimism-sepolia.blockscout.com/tx/0xd679fc3331f3dfb089efde1ad5d04305839e3523f0c441075b8c082b2b6df1d7)
- [recvTx](https://optimism-sepolia.blockscout.com/tx/0xe29b6003c734ec5e14a5712ef5d79bcb0d149b8cb23accb7691995f0550c36e3)