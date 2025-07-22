---
{
  "title": "Privacy and Wasabi",
  "description": "Explanations of common words used in Wasabi and regarding Bitcoin privacy with links to the docs for more details. This is the Wasabi documentation, an archive of knowledge about the open-source, non-custodial and privacy-focused Bitcoin wallet for desktop."
}
---

## Privacy and Wasabi

### #twoweeks

The #twoweeks is a fun inside joke often used in the Wasabi documentation and, more generally, in the Internet community.
In the case of Wasabi documentation, it usually indicates the arrival of a new function or update, to which the future date is still uncertain.

E.g. "Lightning Network is coming to Wasabi in #twoweeks"

### Absolute min input count

The client will refuse to participate in coinjoin rounds with a minimum input count lower than this value.
The default value is 21.

### Address Reuse

Address reuse refers to the use of the same address for multiple transactions, this is very bad for privacy.
Read more: [Address reuse](/why-wasabi/AddressReuse.md)

### Anonymity Score (anonscore)

Anonymity score is a new way to estimate the entropy level of a UTXO in an unequal-but-highly-composable output value coinjoin.
The anonymity score is a metric to help the wallet decide when it's time to stop the coinjoining process.
Read more: [What is the anonymity score?](/FAQ/FAQ-UseWasabi.md#what-is-the-anonymity-score)

### Anonymity Set (anonset)

The anonymity set is effectively the size of the group you are hiding in during a CoinJoin.
It's the quantity of equal value outputs of one CoinJoin transaction.
Read more: [What is the anonymity set?](/FAQ/FAQ-UseWasabi.md#what-is-the-anonymity-set)

### Backend

[The part of a software system that is not usually visible or accessible to a user of that system](https://www.merriam-webster.com/dictionary/back%20end).
In the case of Wasabi, the backend provides the block filters to the [client](/glossary/Glossary-PrivacyWasabi.md#Client).

### Block filters

A filter representing a compact list of addresses in one block.
Wasabi checks locally if any block filter contains transactions with addresses of the wallet.
No public keys are sent to any third party server, thus it is very private.
Read more: [BIP 158: Compact Block Filters for Light Clients](https://github.com/bitcoin/bips/blob/master/bip-0158.mediawiki)

### Blockchain Analysis

Blockchain analysis is used by transaction surveillance companies to follow the transaction history of coins.
Techniques like the common-input-ownership heuristic or change detection are used to create a cluster of transactions belonging to one user.
Read more: [Blockchain Analysis](/why-wasabi/TransactionSurveillanceCompanies.md#blockchain-analysis)

### Bloom Filter

A filter used primarily by SPV clients to request only block headers and merkle proofs of a given transaction from full nodes.
This is very bad for privacy, as third party servers learn about which addresses you are interested in.
Read more: [BIP 37: Connection Bloom Filtering](https://github.com/bitcoin/bips/blob/master/bip-0037.mediawiki)

### Change Address Detection

Many Bitcoin transactions have change outputs.
It would be a serious privacy leak if the change address can be somehow found, as it would link the ownership of the (now spent) inputs with a new output.
Read more: [Change coins](/using-wasabi/ChangeCoins.md)

### Chaumian CoinJoin

A Chaumian CoinJoin is a special type of CoinJoin that utilizes Chaumian [or Schnorr] blind signatures to prevent the central coordinator from spying on the linkage between inputs and outputs.
Read more: [Use of blind signatures in CoinJoin](/using-wasabi/CoinJoin.md#zerolink-protocol-step-by-step)

### Client

[A software that allows a computer to function as a client in a network](https://www.merriam-webster.com/dictionary/client).
In the case of Wasabi, the client is a Wasabi Wallet software version which a user has on his own local machine.
The client can communicate with the [backend](/glossary/Glossary-PrivacyWasabi.md#Backend).

### Cluster

Which entities know about which coins.
For example, this coin belongs to a cluster that is known by a KYC exchange and Alice.
Read more: [What is the cluster history?](/FAQ/FAQ-UseWasabi.md#what-is-the-cluster-history)

### Coin Control

The possiblity for the user to manually select UTXO's.
It is mostly used for sending, so the user can select which UTXO's should be used as the inputs of the transaction.
Read more: [Coin Control Best Practices](/FAQ/FAQ-UseWasabi.md#coin-control-best-practices)

### CoinJoin (CJ)

CoinJoin is a trustless method for combining multiple Bitcoin payments from multiple spenders into a single transaction to make it more difficult for outside parties to determine which spender paid which recipient.
Read more: [What is a CoinJoin?](/FAQ/FAQ-Introduction.md#what-is-a-coinjoin)

### Coinjoin Strategy

A _Coinjoin Strategy_ contains instructions for the automatic "coinjoin robot" about configurations like when and how much to coinjoin.
Read more: [Coinjoin Strategy](/Using-Wasabi/CoinJoin.md#coinjoin-strategy)

### CoinJoined coins

Coins that have successfully participated in a CoinJoin (with the exception of the change) and thus lose their association to a previous cluster.
Read more: [What is the privacy I get after mixing with Wasabi?](/FAQ/FAQ-Introduction.md#what-is-the-privacy-i-get-after-mixing-with-wasabi)

### Common-Input-Ownership heuristic

This is a heuristic or assumption which says that if a transaction has more than one input then all those inputs are owned by the same entity.

### Coordinator

The coordinator is a server which creates CoinJoins and accepts UTXOs in the mix.
Read more: [How does my wallet communicate with the Wasabi coordinator server?](/FAQ/FAQ-UseWasabi.md#how-does-my-wallet-communicate-with-the-wasabi-coordinator-server)

### Daemon

A daemon is a command line interface to run Wasabi without the GUI (Graphical User Interface).
Read more: [Headless Wasabi Daemon](/using-wasabi/Daemon.md)

### Discreet Mode

Discreet Mode is a Wasabi feature that hides sensitive and critical information on the wallet itself, which is useful for screenshots.
Read more: [Discreet Mode](/using-wasabi/DiscreetMode.md)

### Dust

Dust is an UTXO that is uneconomical to spend.
Also, small portions of bitcoin can lead to serious consequences for one's privacy, for example the so called `forced address reuse attack`.
Read more: [What is the dust threshold](/FAQ/FAQ-UseWasabi.md#what-is-the-dust-threshold)

### Know Your Customer (KYC)

KYC (Know Your Customer) is the process of a business being forced to identify and verify the identity of its clients, and to share this information with a government.
The term is also used to refer to the bank regulation which governs these activities.
Read more: [AML/KYC Information](/why-wasabi/TransactionSurveillanceCompanies.md#aml-kyc-information)

### Label

A label can be added to a coin, as a small note on who knows this coin belongs to you.
Good labelling can help the user and the wallet to make better privacy conscious decisions later on when spending.
Read more: [Why do I have to label my address](/FAQ/FAQ-UseWasabi.md#why-do-i-have-to-label-my-address)

### Max Coinjoin Mining Fee Rate

The maximum mining fee rate in sat/vByte the client is willing to pay to participate into a round.
The default value is 150.

### Observers

A way to track who knows about the ownership of your coins.
Not to be confused with a description of a transaction.
Read more: [The importance of labeling](/using-wasabi/Receive.md#the-importance-of-labeling)

### Pay to EndPoint (P2EP)

Pay to EndPoint is when the receiver is reachable over the internet and the sender communicates with the receiver to coordinate a more advanced transaction.
The Tor onion service, IP address or domain of the receiver is included in a BIP21 Bitcoin URI payment link.

### Peers

Peers in our documentation refers mainly to Bitcoin and Wasabi Wallet users, but it also means people.
They are literally peers in the network, or in the CoinJoin.

### RPC

RPC, or Remote Procedure Call, is an interface to interact with Wasabi Wallet programmatically.
Read more: [RPC Interface](/using-wasabi/RPC.md)

### Safety coinjoin

Safety coinjoin is a concept for doing an extra coinjoin after a user registers only _anonymity score_ 1 (non-private) coins in their first round.

This was added in Wasabi [2.0.6 version](https://github.com/WalletWasabi/WalletWasabi/releases/tag/v2.0.6) to increase privacy for people who generate a new wallet -> receive a coin -> do one coinjoin -> send all the money out.
It aims to prevent targeted analysis that compares the value of consolidated coinjoin outputs with the value of one of the coinjoin's inputs.

### Stop coinjoin (Pleb Stop) threshold

The _Stop coinjoin threshold_, a.k.a Pleb Stop, is the confirmed wallet balance under which coinjoin will automatically stop/not start.
The amount can be changed in the _Coinjoin Settings_ (_Stop coinjoin threshold_ setting), the default is 0.01 BTC.

### Taint

Taint is equivalent to the 'trail' that a Bitcoin transaction leaves during the course of its journey.
The taint analysis of a Bitcoin transaction evaluates the association between an address involved in the chain of transactions.
Read more: [Blockchain Analysis](/why-wasabi/TransactionSurveillanceCompanies.md#blockchain-analysis)

### The Onion Router (Tor)

Tor (The Onion Router) is free and open-source software for enabling anonymous communication.
It is widely used by Wasabi.
Read more: [How does Tor protect my network level privacy?](/FAQ/FAQ-GeneralBitcoinPrivacy.md#how-does-tor-protect-my-network-level-privacy)

### Transaction Surveillance Company

A transaction surveillance company is one which attempts to spy on all Bitcoin users.
Their business model is usually to sell the data to any government, corporation or individual willing to pay for their services.
Read more: [Transaction Surveillance Companies](/why-wasabi/TransactionSurveillanceCompanies.md)

### Tumbling / Tumbler

Tumbling is a synonym of 'Mixing'.
Similarly, Tumbler is the synonym of 'Mixer'.

### TurboSync

A feature in Wasabi to reduce wallet loading time.
With TurboSync, some addresses (internal keys only) are skipped and tested in the background.
Read more: [TurboSync](/using-wasabi/WalletLoad.md#turbosync) 

### WabiSabi

WabiSabi is a protocol for constructing coinjoin transactions with the aid of a centralized coordinator.
It utilizes keyed-verification anonymous credentials, homomorphic value commitments, and zero knowledge proofs to achieve privacy and flexibility.
Read more: [WabiSabi](https://github.com/zkSNACKs/WabiSabi/releases/latest/download/WabiSabi.pdf)

### Wallet fingerprinting

A careful analyst sometimes deduces which software created a certain transaction, because many different wallet softwares don't always create transactions in exactly the same way.

### Wasabika

Wasabikas are builders, users and supporters of Wasabi in general.

### XPUB (Extended Public Key)

An xpub, also known as Extended Public Key, is a part of BIP-32 that will allow you to observe your wallet without the private key (xpriv).

### ZeroLink

ZeroLink is a framework to holistically design a privacy and fungibility setup for Bitcoin.
This encompasses more than just a single CoinJoin transaction, but also includes network level privacy defense against third party spying.
Read more: [ZeroLink: the Bitcoin Fungibility Framework](/using-wasabi/CoinJoin.md#zerolink-protocol-step-by-step)
