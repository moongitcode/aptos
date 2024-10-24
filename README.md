# How to build aptos validator
# AIT3
# 1. Run Validator Using Docker
  
## 1-1. Requirements
Refering to formal aptos site.  
https://aptos.dev/nodes/ait/node-requirements  


### 1-1-1. Hardware requirements
  
For running an aptos node on incentivized testnet we recommend the following:  

* CPU: 4 cores (Intel Xeon Skylake or newer)
* Memory: 8GiB RAM
  

### 1-1-2. Storage requirements  
The amount of data stored by Aptos depends on the ledger history (length) of the blockchain and the number of on-chain states (e.g., accounts).  
These values depend on several factors, including: the age of the blockchain, the average transaction rate and the configuration of the ledger pruner.  

We recommend nodes have at least 300GB of disk space to ensure adequate storage space for load testing.  
You have the option to start with a smaller size and adjust based upon demands.  
You will be responsible for monitoring your node's disk usage and adjusting appropriately to ensure node uptime.  
  
### 1-1-3. Networking configuration requirements
For Validator node:  
* Open TCP port 6180, for validators to talk to each other.
* Open TCP port 9101, for getting validator metrics to validate the health stats. (only needed during registration stage)

For Fullnode:
* Open TCP port 6182, for fullnodes to talk to each other.
* Open TCP port 9101, for getting fullnode metrics to validate the health stats. (only needed during registration stage)
* Open TCP port 80/8080, for REST API access.
