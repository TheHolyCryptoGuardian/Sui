# Sui

Sui is the first permissionless Layer 1 blockchain designed from the ground up to enable creators and developers to build experiences that cater to the next billion users in web3. Sui is horizontally scalable to support a wide range of application development with unrivaled speed at low cost.

# What Sui is
Sui is a smart contract platform maintained by a permissionless set of validators that play a role similar to validators or miners in other blockchain systems.

Sui offers scalability and unprecedented low-latency for simple use cases. Sui makes the vast majority of transactions processable in parallel, which makes better use of processing resources, and offers the option to increase throughput with more resources. Sui forgoes consensus to instead use simpler and lower-latency primitives for simple use cases, such as payment transactions and assets transfer. This is unprecedented in the blockchain world and enables a number of new latency-sensitive distributed applications, ranging from gaming to retail payment at physical points of sale.

Sui is written in Rust and supports smart contracts written in the Move programming language to define assets that may have an owner. Move programs define operations on these assets including custom rules for their creation, the transfer of these assets to new owners, and operations that mutate assets.

Sui has a native token called SUI, with a fixed supply. The SUI token is used to pay for gas, and is also used as delegated stake on validators within an epoch. The voting power of validators within this epoch is a function of this delegated stake. Validators are periodically reconfigured according to the stake delegated to them. In any epoch the set of validators is Byzantine fault tolerant. At the end of the epoch, fees collected through all transactions processed are distributed to validators according to their contribution to the operation of the system. Validators can in turn share some of the fees as rewards to users that delegated stake to them.

Sui is backed by a number of state-of-the-art peer-reviewed works and years of open source development.

# Commands for [the Sui node](https://github.com/Avtogen228/Sui/blob/main/Node)

Use `wget -O sui.sh https://raw.githubusercontent.com/Avtogen228/Sui/main/Node && chmod +x sui.sh && ./sui.sh` to install Sui node quickly.

Use `curl -s -X POST http://127.0.0.1:9000 -H 'Content-Type: application/json' -d '{ "jsonrpc":"2.0", "method":"rpc.discover","id":1}' | jq .result.info` to check your node.

Use `journalctl -u suid -f -o cat` to check node logs.

Use `sudo systemctl restart suid` to restart the node.

Use `sudo systemctl stop suid` to stop the node.

Use `sudo systemctl stop suid` then `sudo systemctl disable suid` then `rm -rf ~/sui /var/sui/` and then `rm /etc/systemd/system/suid.service` to delete Sui node.
