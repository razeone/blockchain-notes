## Blockchain

This repo is about notes on the MOOC [Blockchain for Business - An Introduction to Hyperledger Technologies](https://www.edx.org/course/blockchain-business-introduction-linuxfoundationx-lfs171x) by The Linux Foundation.

And other Blockchain personal notes.

## Background - The Rising Interest in Distributed Ledger Technologies

Looking back to the last half century of computer technologies and architectures, one may observe a trend of fluctuation between the centralization and subsequent decentralization of computing power, storage, infrastructure, protocols, and code.

Mainframe computers are largely centralized. They typically house all computing power, memory, data storage, and code. Access to mainframes is mainly by 'dumb terminals', which only take inputs and outputs, and do not store or process data.

With the advent of personal computers and private networks, similar computational capabilities were now housed both on the clients, as well as the servers. This, in part, gave rise to the 'client-server' architecture, which supported the development of relational database systems. Massive data sets, which are housed on mainframes, could move onto a distributed architecture. This data could replicate from server to server, and subsets of the data could be accessed and processed on clients, and then, synced back to the server.

Over time, Internet and cloud computing architectures enabled global access from a variety of computing devices; whereas mainframes were largely designed to address the needs of large corporations and governments. Even though this 'cloud architecture' is decentralized in terms of hardware, it has given rise to application-level centralization (e.g. Facebook, Twitter, Google, etc).

Currently, we are witnessing the transition from centralized computing, storage, and processing to decentralized architectures and systems. According to [Muneeb Ali](https://medium.com/@muneeb/the-next-wave-of-computing-743295b4bc73), these systems aim to "give explicit control of digital assets to end-users and remove the need to trust any third-party servers and infrastructure".

Distributed ledger technology is one of the key innovations making this shift possible.


## Distributed Ledger Technology (DLT)


A **distributed ledger** is a type of data structure which resides across multiple computer devices, generally spread across locations or regions.

**Distributed Ledger Technology** includes blockchain technologies and smart contracts. While distributed ledgers existed prior to Bitcoin, the Bitcoin blockchain marks the convergence of a host of technologies, including timestamping of transactions, Peer-to-Peer (P2P) networks, cryptography, and shared computational power, along with a new consensus algorithm. 

In summary, distributed ledger technology generally consists of [three basic components](https://intelledger.github.io/introduction.html):

* A data model that captures the current state of the ledger
* A language of transactions that changes the ledger state
* A protocol used to build consensus among participants around which transactions will be accepted, and in what order, by the ledger.

## Blockchain Definition

According to [hyperledger.org](https://hyperledger.org/about),

> "A blockchain is a peer-to-peer distributed ledger forged by consensus, combined with a system for "smart contracts" and other assistive technologies."

*Smart contracts* are simply computer programs that execute predefined actions when certain conditions within the system are met.

*Consensus* refers to a system of ensuring that parties agree to a certain state of the system as the true state.

## Blockchain - Block's Anatomy Introduction

Blockchain is a specific form or subset of distributed ledger technologies, which constructs a chronological chain of blocks, hence the name 'block-chain'. A block refers to a set of transactions that are bundled together and added to the chain at the same time. In the Bitcoin blockchain, the miner nodes bundle unconfirmed and valid transactions into a block. Each block contains a given number of transactions. In the Bitcoin network, miners must solve a cryptographic challenge to propose the next block. This process is known as 'proof of work', and requires significant computing power. We shall discuss proof of work in more detail in the Consensus Algorithms section. For a brief history of blockchain technology, please click here.

Timestamping is another key feature of blockchain technology. Each block is timestamped, with each new block referring to the previous block. Combined with cryptographic hashes, this timestamped chain of blocks provides an immutable record of all transactions in the network, from the very first (or genesis) block.

A block commonly consists of four pieces of metadata:

* The reference to the previous block
* The proof of work, also known as a nonce
* The timestamp
* The Merkle tree root for the transactions included in this block.

## Merkle Tree

The Merkle tree, also known as a binary hash tree, is a data structure that is used to store hashes of the individual data in large datasets in a way to make the verification of the dataset efficient. It is an anti-tamper mechanism to ensure that the large dataset has not been changed. The word 'tree' is used to refer to a branching data structure in computer science, as seen in the image below. According to Andreas M. Antonopoulos, in the Bitcoin protocol,

> "Merkle trees are used to summarize all the transactions in a block, producing an overall digital fingerprint of the entire set of transactions, providing a very efficient process to verify whether a transaction is included in a block."

![Merkle Tree](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/5bef2699f0c33f98eb3ccb6c2526b447/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Bitcoin_Block_Data.png)

## Transactions

The record of an event, cryptographically secured with a digital signature, that is verified, ordered, and bundled together into blocks, form the *transactions* in the blockchain. In the Bitcoin blockchain, transactions involve the transfer of bitcoins, while in other blockchains, transactions may involve the transfer of any asset or a record of some service being rendered. Furthermore, a smart contract within the blockchain may allow automatic execution of transactions upon meeting predefined criteria.

*Cryptography* has a key role to play both in the security, as well as in the immutability of the transactions recorded on blockchains. Cryptography is the study of the techniques used to allow secure communication between different parties and to ensure the authenticity and immutability of the data being communicated. For blockchain technologies, cryptography is used to prove that a transaction was created by the right person. It is also used to link transactions into a block in a tamper-proof way, as well as create the links between blocks, to form a blockchain.


## Differences between Blockchains and Databases


Blockchain technology has some key differentiators from databases. 

A blockchain is a write-only data structure, where new entries get appended onto the end of the ledger. Every new block gets appended to the block chain by linking to the previous block's 'hash' (you can check the Glossary tab for a refresher on hash functions). There are no administrator permissions within a blockchain that allow editing or deleting of data.

In a relational database, data can be easily modified or deleted. Typically, there are database administrators who may make changes to any part of the data and/or its structure. Additionally, blockchains were designed for decentralized applications, whereas relational databases, in general, were originally designed for centralized applications, where a single entity controls the data.

![Differences DB vs Blockchain](https://prod-edxapp.edx-cdn.org/assets/courseware/v1/d387060c18e43cb6f676f10c56443ce7/asset-v1:LinuxFoundationX+LFS171x+3T2017+type@asset+block/Centralized_Databases_vs_Blockchain.png)