---
title: "Introduction to the Lightning Network"
date: 2021-06-09T10:07:21+06:00
# post image
image: "https://raw.githubusercontent.com/shocknet/bitcoin-lightning-logo/master/LOGO-01.png"
# post type (regular/featured)
type: "regular"
# meta description
description: "This is meta description"
# post draft
draft: false
---

## The scalability problem

Bitcoin can only work because all participants in the network (not just miners but also economic actors) can independently verify
that every transaction that has happened since 2009 happened correctly. Everyone can verify the total supply of Bitcoin, and verify that what they have in their wallet actually belongs to them and only to them. This is extremely important because if we were to compromise on this feature, we would allow trust to be reintroduced into the system, making everything just a bad clone of already existing financial institutions. 

Every block thus contains a number of transactions that will have to be reprocessed by everyone, *forever*. If you start now and want to verify the entire system, starting from 2009, you would need several days of computing power on a high-end computer (note that this has nothing to do with mining).

Because of this, there is a limit on how much data can be included in a block, which is about 3.7 MB. This ensures that future participation in the Bitcoin network will still be possible for everyone. You might say that computers will become faster, but Moore's law is soon coming to an end because chip manufacturers are already at intrinsic physical limits on how small they can build chips. If everyone uses the base chain for every transactions, the requirements for participating in the network would soon become absurdly high. So, it makes no sense to use the base chain for "small" value transactions.

## Fees
Because blockspace is limited to a maximum of about 3.7MB every 10 minutes, everyone who wants to make a transaction needs to place a *bid* in order to "bribe" the miners into including their transaction in a block. Naturally, miners will include transactions that are willing to pay a higher fee, and this means that from time to time, Bitcoin transactions can be really expensive.

![](../../images/johoe.png)

This culminated in 2017 when transactions fees where in the range of $50 to $100 for weeks at a time. Since then, the ecosystem has adopted more and more scaling solutions like Segwit, transaction batching and the Lightning Network, which has resulted in significantly lower fees and less pressure on the base chain, even as the Bitcoin price rallied significantly in 2021. If Bitcoin were to become more widely adopted however, fees could rise again, and that's why it's important to use technologies such as the Lightning Network.

## Lightning

The Lightning Network is based on an invention by Joseph Poon and Thaddeus Dryja which is called a "payment channel".

![](../../images/channel-naive.png)

In this channel, both parties (say a normal user, Bob, and his Bitcoin-savvy aunt, Alice), place their bitcoin inside a special transaction called a multi-signature transaction. This means that these funds can only be spent if they both sign it with their digital signature. They could make transactions between them, constantly updating their balances but never telling the rest of the world about these updates. Then, after a while if they decide to part ways, they can broadcast the final state to the network and get on with their lives.

However, this reintroduces the old problem: double spending. What if Bob and Alice update their channel to indicate that Bob has sent money to Alice, but then Alice decides to broadcast the *old* state to the network? We need something to make sure that Alice cannot do this.
![](../../images/channel-better.png)


Poon-Dryja payment channels introduce a mechanism where with every update, a secret is revealed that invalidates the old state of the transaction. If one party then decides to cheat, the other party can prove to the network that a cheat has occured by providing the secret. This makes channel updates trustless.

## Lightning Network

Payment channels between 2 parties are interesting, but are not extremely useful. Lightning is however a *Network*, made out of thousands and thousands of these channels. You can pay anyone on the network, even if you have only 1 channel with 1 other person, provided that this person is connected to other people on the network. Like this, all you have to do in an ideal case, is only do 1 transaction on-chain, which you can then use an unlimited amount of times and never close. Constructed like this, Lightning allows Bitcoin to scale to an enormous amount of transactions without compromosing on the things that make it valuable.

Please consult this [page](https://www.lopp.net/lightning-information.html) if you want to learn more about LN.
Below, you can watch another explanation on the Lightning Network and also find tutorials on how to use some of the more popular Lightning wallets, Phoenix Wallet and Breez Wallet.
## A deep-dive explanation by Andreas Antonopoulos
{{< youtube XCSfoiD8wUA >}}

## Wallet tutorial: Phoenix Wallet
{{< youtube Cx5PK1H5OR0 >}}
## Wallet tutorial: Breez Wallet
{{< youtube t_4b-y4T8bY >}}


