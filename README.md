

# **Alice's Deposit - Proxy RPC**

**Privacy is not an option**

In an increasingly interconnected Blockchain ecosystem, it has become challenging to disentangle your on-chain activity from your identity. To avoid being associated with a specific address or transaction, we need the capability to interact with the blockchain privately. Here is the solution we have developed to solve this issue.

####

## **Features** ✨

- A fully private and decentralized RPC caller 🌐
- Private RPCs based on the [Hopr network](https://hoprnet.org/)   <img src="https://s2.coinmarketcap.com/static/img/coins/200x200/6520.png"  height="20">
- Hosted on [bacalhau](https://www.bacalhau.org/) <img src="https://pbs.twimg.com/media/FTNDJSrXwAE8jCz.jpg" width="20" height="20">

## **The concept** 💡
Our solution provides users of centralized exchanges with a way to withdraw funds while keeping their physical identity separate from the final receiving address. However, when a user employs a public RPC provided by a tier to make a transaction on a blockchain, let's say a ZKBOB direct deposit or a withdrawal, their address will be linked to the IP address making the request. This IP address is often the user's own, revealing their identity. This is where Hopr RPCh comes in: it effectively conceals the user's IP address from the RPC. Hopr RPCh is deployed on Bacalhau and is a valuable tool for maintaining user privacy.


## **How we built it** 👨‍💻
The RPCh lives on Bacalhau, to launch the workload, run the command:
```bash
bacalhau docker run -e RESPONSE_TIMEOUT=10000 -e DISCOVERY_PLATFORM_API_ENDPOINT=https://production.discovery.rpch.tech -e PORT=8080 -e DATA_DIR=app -e CLIENT=arrow-worried-little-of-private  europe-west6-docker.pkg.dev/rpch-375921/rpch/rpc-server:latest
```
You should buy able to connect to the RPC using this endpoint : http://<machineIP>:8080/?exit-provider=<providerOfYourChoice> 

## A huge thanks to the Filecoin team to have accepted our whitelist request for the https://production.discovery.rpch.tech endpoint 

## **The team** 🏆

**The team consists of 4 committed people who love what they do.**

We are all students bound by our passion and commitment for blockchain and Web3. We want to develop innovative solutions that will help the whole ecosystem expand. Too many times have we seen privacy being set aside in projects and we want to be able to change that. That is why Maxime, Nathan, Thomas and Adam are glad to present Alice’s Deposit, the solution for real privacy.

By addressing the need for privacy in the blockchain ecosystem while having a real utility in our daily life, Alice's Deposit has the potential to be a valuable tool for individuals and businesses alike.


## **Contribute** 📚

Our project is intended as open source and as a tool for the Ethereum community and all web3 users.

Feel free to contribute!

**Maxime - Thomas - Nathan - Adam**
