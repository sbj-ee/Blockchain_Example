# Blockchain Example

A simple blockchain implementation in Python for educational purposes.

## Installation

```bash
python3 -m venv .venv
source .venv/bin/activate
# No external dependencies required
```

## Features

- Block creation with SHA-256 hashing
- Proof-of-work mining with configurable difficulty
- Transaction management
- Chain validation

## Usage

```bash
python bc_example.py
```

## How It Works

### Block Structure

Each block contains:
- `index`: Position in the chain
- `transactions`: List of transaction data
- `timestamp`: Block creation time
- `previous_hash`: Hash of the previous block
- `nonce`: Number used for proof-of-work
- `hash`: SHA-256 hash of the block

### Mining

Blocks are mined using proof-of-work. The miner must find a nonce that produces a hash starting with a specified number of zeros (difficulty level).

### Example Output

```python
bc = Blockchain()
bc.add_transaction("Alice sends 10 to Bob")
bc.add_transaction("Bob sends 5 to Charlie")
bc.mine_pending_transactions()

print("Valid:", bc.is_valid())  # True
```

## Requirements

- Python 3.x
