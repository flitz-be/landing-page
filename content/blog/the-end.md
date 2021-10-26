---
title: "Alles hat ein Ende"
date: 2021-10-26T10:07:21+06:00
# post image
image: "../../images/thats-all.webp"
# post type (regular/featured)
type: "featured"
# meta description
description: "So long and thanks for all the fish."
# post draft
draft: true
---

Dear Flitz customers,

It is with a heavy heart that I stand before you today to announce the end of the Flitz platform. I know most of you will be quite disappointed in hearing this, because over the last couple of months I have received an overwhelmingly positive feedback on Twitter. I hope that you will all understand after reading this post.

## Background
I discovered bitcoin and the Lightning Network in 2017. From the moment I read about this on Reddit, I was completely hooked. Bitcoin by itself as a "savings technology", a "store of value" never interested me that much. Don't get me wrong, I agree with the premise. There is tremendous value in a "digital gold" that has monetary rules set in stone. But it became clear to me that without Lightning, use-cases would be limited and those who need it most wouldn't be able to benefit from it. No, what interested me was the Lightning Network. Instant transactions for less than a cent. Re-architecting the internet and getting rid of the ads, and introduce a fair monetization system for creators. No more asking payment processor X if they will pretty please allow you to start your business. I became a Lightning Network maximalist. I believe that in the future, at least 90% of on-chain transactions will be splices from one channel to another. I took my first job back in 2018 at a company that used Go for the back-end, because I knew that was what LND was written in.

The idea for Flitz started in 2019. From EUR on your bank account to BTC on the Lightning Network in the fastest and most user-friendly way possible.
I focused on this core product which meant *not* creating a custodial wallet: there are dozens of (non-/semi-)custodial wallets already on the market, made by people who know what they are doing, it didn't make any sense for me to start making one myself. Using LNURL-withdraw (the most important invention since LN itself), the Flitz app could make the whole process so seamless, all while being natively non-custodial. The emergence of wallets like Phoenix and Breez meant that you didn't need your own node in order to use Lightning in a non-custodial way, and Flitz was able to leverage this because all these wallets speak the LNURL-withdraw protocol.

## Why it's over
I only worked full-time on the project earlier this year. I had a day-job before that and started another one during the summer. However, it became mentally difficult, not to say almost impossible, to combine running Flitz with another job. That's why earlier this month I decided to give up my other commitment and once again put all my energy in Flitz. However, soon after it became clear that it was an impossible task to continue the entire project on my own. The mental burden became so big that I couldn't get any more work done, and I started feeling physically ill because of the stress.

What I wanted to do is build cool things on top of Lightning. What I ended up doing was:

- Studying [Belgian AML/CFT regulation](https://www.ejustice.just.fgov.be/cgi_loi/change_lg.pl?language=nl&la=N&table_name=wet&cn=2017091806), and crafting an AML/CFT policy in accordance with it
- Implementing systems to enforce above-mentioned policy, eg. doing customer due diligence
- Filling out forms
- Doing customer support
- Juggling money around bank accounts, exchanges and the LN node
- Trying to figure out the accounting side of this whole operation

People have encouraged me to turn Flitz into a "real startup": find a co-founder, raise money from investors, hire people, ...
I am not going to do this because I don't want to. Starting a company is not about coding, engineering, or Lightning.
It's about having a vision. And it's about getting people (co-founders, investors, employees) to believe in this vision. So it's really about people.

I don't have a vision. I have some vague ideas about what the future should look like, and all of them involve the Lightning Network. I want to solve problems using software. I wanted to build something cool on Lightning, something that I would use myself if I discovered Lightning today. Mission accomplished.
## What we achieved
Over the course of 3 months, hundreds of users have pumped almost 100.000 EUR straight into the Lightning Network. People would transfer 5 EUR every day and DCA it straight into their _own_ lightning nodes. People have sent 1000 EUR at once and withdrawn it without any issue at all. I think we can say Flitz has been a small part of Lightning history, showing what's possible if you fully embrace it's power.
## The future

**The Flitz app is not going to disappear.** You can continue to open it, and Android will even get an update. **You will be able to export all your transactions**, a feature that was asked by many. Below you can find a timeline.
**If you have any recurring payments to Flitz, please stop them as soon as possible.**

- 29/10 Blog post published, Play Store links removed from site. New sign-ups will be halted, SEPA deposit information will be removed from the app.
- 8/11 00:00 CET Incoming SEPA deposits won't be processed anymore and will be sent back.
- 25/12 New feature: exporting transactions
- 31/12 Withdrawals halted

As for me, it's back to normie life for a while. I have more ideas though. I want to contribute to some open source projects that made Flitz possible. And why not an open-source, self-hosted version of Flitz? With more and more exchanges supporting Lightning (shout-out [Okcoin](https://okcoin.com)!), possibilities open up to make some real cool, completely self-hosted stuff. Maybe a new generation of the Flitz app connects to your own back-end infrastructure, exchange or node. BOLT12 and LN Address will completely transform how we use Lightning, and I certainly want to build more stuff using those technologies.

I'm also available to give presentations, workshops, or consultancy on Lightning or running (C-) Lightning in the cloud. Not full-time though, I need a normie job to get back to my senses.


Peace out,

Kwinten
