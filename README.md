# Guide-0g-da-Node

# Hardware Requirement
```bash
- Memory: 16 GB
- CPU: 8 cores
- Disk: 1 TB NVME SSD
- Bandwidth: 100 MBps for Download / Upload
```

# Installation
```bash
git clone https://github.com/0glabs/0g-da-node.git
cargo build --release
./dev_support/download_params.sh
```

# Configuration
Create a config.toml file

```bash
log_level = "info"

data_path = "./db/"

encoder_params_dir = "params/" 

grpc_listen_address = "0.0.0.0:34000"

eth_rpc_endpoint = "https://rpc-testnet.0g.ai"

socket_address = "<public_ip/dns>:34000"

da_entrance_address = ""

start_block_number = 0

signer_bls_private_key = ""

signer_eth_private_key = ""

enable_das = "false"
```

```bash
cargo run --bin key-gen
```

# Run
```bash
./target/release/server --config cargo.toml
```
