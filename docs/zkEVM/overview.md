Polygon zkEVM is to Ethereum a Layer 2 network and a scalability solution utilizing zero-knowledge technology to provide validation and fast finality of off-chain transactions.

Polygon zkEVM supports a majority of Ethereum EIPs, precompiles, and opcodes. Developers benefit from the seamless deployment of smart contracts, developer tools, and wallets that already work on Ethereum, but in an environment with significantly lower costs.

## Protocol development highlights

The Polygon zkEVM testnet launched with a complete ZK proving system and full transaction data availability in October 2022. The proving system uses a combination of eSTARK proofs and FRI, that are then compressed using FFLONK SNARKs to create the final ZK proof.

Following the launch of the testnet, the code base for Polygon zkEVM underwent several security audits. These were among the first audits ever performed on a complete, in-production ZK proving system.  

After the audits, Polygon zkEVM Mainnet Beta [launched in March 2023](https://www.youtube.com/watch?v=UvQIX5i09A4&ab_channel=ETHGlobal). Since then, the zkEVM network has had two major upgrades: [Dragon Fruit (ForkID5)](https://polygon.technology/blog/polygon-zkevm-dragon-fruit-upgrade-with-new-opcode-coming-to-mainnet-beta), in September 2023, and [Inca Berry (ForkID6)](https://polygon.technology/blog/polygon-zkevm-inca-berry-upgrade-coming-to-mainnet-beta), in November 2023.

All updates and upgrades of both the mainnet and testnet can be found in the [Historical data document](../zkEVM/get-started/historical-data.md).

## Security measures

zkEVM's upgrades are on par with Ethereum's security standards as they involve deployment of the following contracts:

- An admin multisig contract to avoid having one account controlling upgrades.
- A timelock contract to give users sufficient time delay to withdraw before execution.
- A transparent upgradeable proxy, from OpenZeppelin’s libraries of audited and battle-tested contracts.

The activation of the 10-day timelock for upgrading zkEVM's smart contracts on Ethereum requires approval by the network's [Admin](https://etherscan.io/address/0x242daE44F5d8fb54B198D03a94dA45B5a4413e21), a three-participant multisig that acts as a [governance tool](../zkEVM/architecture/protocol/admin-role.md#governance-of-zkevm-contracts) for the protocol. This is a Gnosis Safe with a 2/3 threshold.

In the event of an emergency that puts user funds at risk, the network's [Security Council](https://etherscan.io/address/0x37c58Dfa7BF0A165C5AAEdDf3e2EdB475ac6Dcb6) may remove the 10-day timelock. In such an emergency, the network state stops advancing and bridge functionality is paused. The Security Council is an eight-participant multisig. This is a Gnosis Safe with a 6/8 threshold. Learn more about [zkEVM upgradability](https://docs.polygon.technology/zkEVM/architecture/protocol/upgradability/).

