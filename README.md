Blockchain Example
A simple, educational blockchain implementation in Rust that demonstrates core blockchain concepts including transactions, proof-of-work mining, and blockchain validation.
Features

Create and process transactions between users
Mine blocks with proof-of-work algorithm
Verify blockchain integrity
Mine pending transactions with mining rewards
Save/load blockchain state to/from disk
Command-line interface for interacting with the blockchain

Prerequisites

Rust (latest stable version)
Cargo (comes with Rust)

Installation

Clone the repository:
bashgit clone https://github.com/yourusername/blockchain-example.git
cd blockchain-example

Build the project:
bashcargo build --release


Usage
Run the application:
bashcargo run
Available Commands
The interactive CLI provides the following options:

Add Transaction - Create a new transaction between users
Mine Transactions - Process pending transactions and add them to a new block
View Blockchain - Display the current state of the blockchain
Validate Blockchain - Check if the blockchain is valid
Save Blockchain - Save the current blockchain state to a file
Load Blockchain - Load a blockchain state from a file
Exit - Terminate the application

Architecture
Core Components

Block (block.rs) - Represents a single block in the blockchain

Contains transactions, timestamp, hash, and proof-of-work data
Implements mining functionality with adjustable difficulty


Transaction (block.rs) - Represents a transfer of value between users

Tracks sender, recipient, and amount


Blockchain (blockchain.rs) - Manages the chain of blocks

Maintains a list of pending transactions
Validates the integrity of the chain
Handles persistence (save/load functionality)



Technical Details
Proof of Work
The blockchain uses a basic proof-of-work algorithm similar to Bitcoin's. Miners must find a hash with a specific number of leading zeros, determined by the difficulty setting. This is achieved by incrementing a nonce value until a valid hash is found.
Data Persistence
Blockchain state can be saved to and loaded from JSON files, enabling the application to maintain state between sessions.
Security
The implementation includes basic blockchain validation that checks:

The integrity of each block's hash
The continuity of the chain (each block references the previous block's hash)

Examples
Adding a Transaction
Choose an option:
1. Add Transaction
Enter sender:
alice
Enter recipient:
bob
Enter amount:
10.5
Transaction added!
Mining Transactions
Choose an option:
2. Mine Transactions
Enter miner address:
minerAddress123
Transactions mined!
License
MIT License
Acknowledgments
This project is for educational purposes to demonstrate blockchain concepts. It is not intended for production use.