---
title: "If you don't get it or don't understand, I'll try to explain it to you."
date: 2021-06-08T10:07:21+06:00
# post image
image: "../../images/mim.jpeg"
# post type (regular/featured)
type: "regular"
# meta description
description: "If you don't understand or don't get it, read this post."
# post draft
draft: false
---

## What is it

The main thing to understand about Bitcoin is that it has both properties of a physical *thing* and digital *information*.

This means that you can *own* it in the same way that you own your physical possessions. It could even be argued that ownership is even *stronger* in the case of BTC, as the private key (under the form of 12 or 24 secrets words) can be stored inside your head. Someone could show up at your house with a police escort and take everything you have, but if you have properly secured your Bitcoin, they won't be able to take it from you.

![](../../images/seed.png)

So, having a secret key (under the form of a set of 12 random words) means that you have control over a certain amount of Bitcoin. These coins are "located" everywhere and nowhere. Every node on the Bitcoin network stores them, but nobody can *control* them except the person or persons knowing the secret. When you give in the secret in your wallet (always be very careful when doing this!), the secret is not sent to anyone over the internet. Instead, a list of *addresses* is derived from this secret **on your local device**, and then your wallet software asks different nodes on the network how much money is on these "addresses". Like this, you and only you are the one in control of your money.

## Double spending - the problem

The system explained above might sound cute, but a problem appears to arise once you decide to *send* your bitcoin to someone else. Since there is no central authority in the system, who is determining the *order of transactions* ? Say I decide to send you some bitcoin:

1. You generate an address from your secret and give it to me.
2. I construct a transaction that says: move 0.01 bitcoin from address A to address B.
3. I sign this transaction with a digital signature, using the secret that's behind address A. That proves that I have control over the funds locked in address A.
4. I broadcast this transaction to everyone on the network, so everyone knows I did this.

![](../../images/doublespend.jpg)

Case closed you think? What if I, at the same time of doing step 4, also broadcast another transaction: one that sends the funds not to address B, but to address C, that I also happen to control? How is anyone else going to determine what the "real" transaction is? I might tell people in Europe about transaction 1 but tell people in America about transaction 2. In a distributed system without central authority, there is no way of knowing the "correct" order of these transactions.

## Double spending - the solution

The solution to this problem is (as strange at it might sound) an election. Everyone has a chance to vote on the order of transactions. You and I, when doing bussiness, agree that the outcome of this vote is what will determine if I have actually paid you or not. 

At first sight, this seems absolutely stupid. Without a central authority, who will stop people from voting twice, or a billion times? Who will decide when the election is over and we can get on with our lives? This is where the real innovation in Bitcoin lies: Proof of Work. PoW means that everyone gets a percentage of the votes in accordance with how much computing power they control in relation to everyone else. If you control 50% of the "hashpower", you get 50% of the votes. The crucial part of the system is that everyone can verify independently how much computing power someone has without relying on a central authority. Everyone who wishes to participate in this system is free to do so. This "election" is held every 10 minutes and results in what is called a "block". If your transaction is included in a block, you can be relatively sure to regard it as final. To reverse the transaction, an attacker would need to spend considerable resources to attack the network, which is possible in theory, but is not economically rational in practice if their rewards for doing so would be less than the resources spent. Every block added to the network adds to it's security, and after 6 confirmations (about 1 hour), practically every transaction can be considered absolutely final.

![](https://upload.wikimedia.org/wikipedia/commons/7/7a/Bitcoin_Block_Data.png)
It's important to stress again that the only thing miners vote on is the *order* of transactions. They are rewarded for this through newly minted bitcoins and through transaction costs. This is why "blockchain" projects that do not have a "money" attached to them make no sense, because in that case there is no incentive for the miners to "do the right thing" and keep the system honest.

If you want to learn more about Bitcoin, please check out [Jameson Lopp's documentation](https://lopp.net/bitcoin.html).

In the next article we will talk about the scalability problem and about a possible solution: the Lightning Network.