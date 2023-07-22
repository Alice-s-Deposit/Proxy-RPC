

# **Alice's Deposit - Proxy RPC**

**Privacy is not an option**

In an increasingly interconnected Blockchain ecosystem, it has become challenging to disentangle your on-chain activity from your identity. To avoid being associated with a specific address or transaction, we need the capability to interact with the blockchain privately. Here is the solution we have developed to solve this issue.

####

## **Features** ✨

-  A fully private and decentralized RPC caller 🌐
- API caller built on [bacalhau](https://www.bacalhau.org/) <img src="https://pbs.twimg.com/media/FTNDJSrXwAE8jCz.jpg" width="20" height="20">
- Private RPCs based on the [Hopr network](https://hoprnet.org/)   <img src="https://s2.coinmarketcap.com/static/img/coins/200x200/6520.png"  height="20">

## **The concept** 💡
When a user wants to withdraw funds from a centralized exchange, they can use our solution to ensure that their final receiving address is not linked to their physical identity. However, as soon as they use a public RPC (Remote Procedure Call), their address will be identified as belonging to them. This is where our proxy comes in handy: it makes the RPC call private using a container on bacalhau and hopr.


## **How we built it** 👨‍💻
 L'api caller tourne dans un container docker et est initialisé par la commande:
```bash
docker run -e RESPONSE_TIMEOUT=10000 -e DISCOVERY_PLATFORM_API_ENDPOINT=https://production.discovery.rpch.tech -e PORT=8080 -e DATA_DIR=app -e CLIENT=moon-science-statement-government-off --name rpc-server -p 8080:8080 --rm --pull=always europe-west6-docker.pkg.dev/rpch-375921/rpch/rpc-server:latest
```

Une fois que notre demande de whitelist pour le endpoint `https://production.discovery.rpch.tech` a du été acceptée par filecoin.

La dernière étape consiste à lancer Bacalhau:
```bash
bacalhau run command.sh
```

command.sh :
```bash
docker run -e RESPONSE_TIMEOUT=10000 -e DISCOVERY_PLATFORM_API_ENDPOINT=https://production.discovery.rpch.tech -e PORT=8080 -e DATA_DIR=app -e CLIENT=moon-science-statement-government-off --name rpc-server -p 8080:8080 --rm --pull=always europe-west6-docker.pkg.dev/rpch-375921/rpch/rpc-server:latest
```

The api should be up and running on port 8080 !


## **The team** 🏆

**The team consists of 4 committed people who love what they do.**

We are all students bound by our passion and commitment for blockchain and Web3. We want to develop innovative solutions that will help the whole ecosystem expand. Too many times have we seen privacy being set aside in projects and we want to be able to change that. That is why Maxime, Nathan, Thomas and Adam are glad to present Alice’s Deposit, the solution for real privacy.

By addressing the need for privacy in the blockchain ecosystem while having a real utility in our daily life, Alice's Deposit has the potential to be a valuable tool for individuals and businesses alike.


## **Contribute** 📚

Our project is intended as open source and as a tool for the Ethereum community and all web3 users.

Feel free to contribute!

**Maxime - Thomas - Nathan - Adam**
