# Nonce
Project Nonce aims to build an indexer of the decentralized web that runs in a decentralized way.

## Inspiration
Next generation web is being built on top of a peer to peer network. Maintaining the index of each data in such an environment, however, is rather complicated. Unless the creator of data notifies the network, whether by protocol or not, it shall not be easy to know which data has been registered. Thanks to the design of the protocol and a few mechanisms that are designed to help us easily identify the resources, the idea of monitoring and scraping the network seems viable.

## Target Systems
- Ethereum
- Interplantery File System (IPFS)

## Crawling
There are a few ways we can walk on the network.

**Iterating Ethereum Name Service (ENS)**
Ethereum Name Service (ENS) is devised to help people use human-readable names to signifiy long hexadecimal values. Those values might be content identifiers on the IPFS. ENS in this sense can serve as a giant map of a part of IPFS. Nonce collects content hashes from ENS and access those that match on IPFS.

**Tapping on Gossipsub**
Libp2p, the underlying technology that powers IPFS, has a mechanism to circulate messages among peers. This message contains the information such as which file has been seen. Leveraging this in a scalable manner can be a key to creating an index of the network.

## The issue of "who will execute"
Nonce looks to build **a decentralized system of indexing the decentralized web**. For it, we propose a way to allow peers to undertake crawling. **Rand** is a subsystem on top of Ethereum that collaboratively selects a random peer to delegate works.

## Components
- crawler https://github.com/decentralized-web-indexer/dwi-crawler
- web application https://github.com/decentralized-web-indexer/webapp
- work delegation https://github.com/eldeni/verifiable-computing
