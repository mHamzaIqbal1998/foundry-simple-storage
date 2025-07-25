## Foundry Simple Storage

This project demonstrates a simple storage smart contract using [Foundry](https://book.getfoundry.sh/). It includes everything you need to deploy and interact with the contract on Ethereum testnets.

### Prerequisites

- [Foundry](https://book.getfoundry.sh/getting-started/installation) (includes `forge`, `anvil`, and `cast`)
- An Ethereum RPC URL (e.g., Sepolia testnet)
- A funded wallet/private key

### Setup

1. **Import your wallet using `cast`:**

   ```sh
   cast wallet import <wallet-name> --interactive
   ```

   This will securely store your private key for use with Foundry scripts.

2. **Deploy the contract:**

   Replace the following placeholders:
   - `<WALLET_NAME>`: The name you used when importing your wallet
   - `<SENDER_ADDRESS>`: The address of your wallet
   - `<SEPOLIA_RPC_URL>`: Your Sepolia (or other testnet) RPC endpoint

   Then run:

   ```sh
   forge script script/DeploySimpleStorage.s.sol \
     --rpc-url $SEPOLIA_RPC_URL \
     --account <WALLET_NAME> \
     --sender <SENDER_ADDRESS> \
     --broadcast
   ```

### Notes

- Make sure your wallet has testnet ETH for gas fees.
- You can modify the deployment script or contract as needed for your use case.

For more information, see the [Foundry Book](https://book.getfoundry.sh/).