# Blockchain and Cryptocurrency for Beginners

## Introduction
Anyone who has carried out even light sleuthing about the hot topics of Computer Science on the Internet is bound to have come across terms such as Blockchain, cryptocurrencies, mining, etc. These concepts form an inter-connected network that may seem daunting to comprehend at first. However, some dedicated reading will expose a perfect harmony between several fields of Computers that have revolutionized our approach and countless walks of life. Before diving into the depths of this technology, let’s begin with some history.
The concept of cryptocurrencies is not a new one. For decades, people have been trying to make headway into this technology, with varying levels of success. One of the prominent hurdles is a lack of consensus between involved parties. In simple terms, if two parties carry out a transaction, the history of the transaction must be recorded by all members on the system. However, if any two parties have different records, which one should be accepted? This disparity has in turn prevented cryptocurrencies from bursting onto the scene for several years.
Blockchain

* The Birth of Blockchain
The solution to this problem was found not too long ago by a person or group of people named Satoshi Nakamoto in 2009 who released a paper outlining a cryptocurrency called Bitcoin, along with its method of implementation. Surprisingly, the identity of Satoshi Nakamoto remains a mystery to this day. But for all the mystery buffs, there are unconfirmed reports that USA’s Homeland Security has identified him! 
Of interest to us, is the underlying construct used for the implementation of this novel cryptocurrency concept. This construct has eventually been termed Blockchain (the explanation of its design in subsequent sections will explain the choice of name). The concept of a secure and accountable cryptocurrency and the near limitless potential of the underlying Blockchain technology itself have captured the imagination of one and all. To describe it as simply as possible, Blockchain is a trustless, immutable and decentralized, distributed ledger. Too many adjectives? Let’s examine it in more detail.

*	Ledger
At its very core, Blockchain is simply a ledger. It keeps track of all transactions taking place on its network so that there is a complete recorded history of all currency movements across it. As a result, no one can back out of a transaction they have carried out, or fake a transaction for their own benefit. An accurate and trustworthy ledger of all transactions also facilitates tracking down fraudulent users.

*	Decentralized and Distributed
While the above model has been attempted before, in the past, the control of the ledger always had to be placed in the hands of some trusted central authority. Every time a member needed information about the current history of transactions, they’d have to request it from said authority. This implied that the authority was impartial, but if they were to become corrupt or malicious and alter the ledger, the entire system would be compromised. This in itself represented a great security risk. 
Blockchain however, has found a way to work around this inherent bias through a strategy of decentralization and distribution. Put simply, there is no longer a central authority in the picture and each participant has their own copy of the ledger. Every time a transaction is initiated, it is verified by other members of the network basis several parameters. Once confirmed, everyone’s copy is updated with this transaction. This ensures that at all times, every participant in the system is aware of all valid transactions. This in turn, reduces chances of fraud, as every member is privy to transactions which are verified and authenticated, as well as to those which cannot be trusted.

*	Trustless
Next comes the aspect of trust factor. In a conventional “trust-based” business model of the past, when parties carried out transactions online (or in some cases, even offline), a trusted Third-Party was required to verify the authenticity of the members involved and of the transaction itself. This once again posed a security risk (similar to placing the ledger in the hands of a central authority). Blockchain on the other hand, is trustless i.e., no such third party is needed. Members of the system itself perform all necessary verifications and authentications of any transaction, before appending it to every member’s ledger. The system also keeps track of each transaction’s verifier. Thus, if a fraudulent transaction is verified, once it is identified, its verifier can easily be penalized, sometimes even booted from the network.

*	User Anonymity
As part of implementation of cryptocurrencies, a key feature was for each member of the network to remain anonymous, as otherwise everyone would know the identity of the participants of any given transaction. This posed a challenge as there was no way to verify the identity of people joining the network. Literally anyone with a computer and an Internet connection (including malicious users intending to corrupt the system) could participate (the effects of this downside are still felt today, as cryptocurrencies are heavily used in black market trade). All they had to do was broadcast a fraudulent transaction of valid design to some user, and his/her ledger would get updated with this transaction. Satoshi managed to effectively resolve this problem, which be addressed in greater detail in the latter part of the blog.

* Need for Immutability
There was another major issue that had to be addressed. What if someone were to manually rewrite a certain transaction, which in turn got updated in everyone’s ledgers? This emphasized the need for the property of immutability i.e., there had to be a way to prevent user/s to alter a transaction once it was added to the ledger.
Taken together, the above features provide a high-level view of Blockchain’s features. In order to fully comprehend Satoshi’s solutions for Consensus and immutability problems mentioned earlier, we need a deeper understanding of the working of Blockchain.

*	Transaction Validation
Let’s begin with how transactions are initiated and verified. Since users are anonymous, they require a method to identify themselves and carry out transactions. This is implemented using a concept called Public-Key Cryptography. Each user is given a public-private key pair, and a freshly generated address. The public key is visible for all to see, but the private one must be kept secure, as it basically functions as the master controls to the account. The pair works in such a way that messages encrypted using one member of the pair can only be decrypted using the other. 
When a user initiates a transaction, he encrypts it with his/her private key to produce what’s called a Digital Signature. He then encrypts it again with the recipient’s public key, and sends it. The recipient now uses his own private and the sender’s public key to obtain the transaction message, thus accurately verifying its contents and the sender as well. 

*	Miner Nodes
Once a transaction is verified, the users (also called nodes of the network) broadcast it to the rest of the network, wherein it’s picked up by special nodes called Mining Nodes.
Transactions aren’t simply stored in a sequential order in the ledger. They are compiled into chunks of transactions called blocks. This compilation is carried out by miners. They are special nodes whose job is to listen for transactions and further validate them on the basis of a few more parameters. They then send these transactions into transaction pools. From here, other miners can pick up the ones they want and begin the process of compilation. There is a limit to the number of transactions per block, generally fixed for a given system. 

*	Mining
While creating the block, the miner adds a special transaction of his own as the first one, called coinbase transaction. This represents his payment for compiling the block, and provides miners with incentive to continue mining. This is called miner’s fees. As the payment comes not from any particular user, but from the system itself, it results in the production of fresh coins (the units of the concerned cryptocurrency). This process is known as mining. Every cryptocurrency has a fixed total rate of mining. This number is halved once every 4 years or so in the case of Bitcoin, and reports show that at the current rate, Bitcoin mining will cease around the year 2140.

*	Issues That Arise During Mining
Getting back to the mining itself, once the miner adds all necessary transactions to the block, he adds some additional information like block number, number of transactions, etc. and the block is ready to be appended to every member’s ledger. At this stage of the process, we encounter two new problems.
Firstly, we have a large number of miners working on the same transaction pool. If multiple miners happen to mine the same set of transactions, which of them should get the miner’s fee? We need some way to clearly ascertain which miner ‘finished first’, so to speak.
Secondly, what if a malicious miner decides to create a block filled with fraudulent transactions, and then broadcast it? As of now, there’s nothing stopping him from doing so. Thus, we need some way to make the creation of blocks ‘computationally expensive’, so that it would require great investment of money and time to cheat the system.

*	Proof of Work
These problems were together solved by a concept known as proof of work. To put it in simple terms, once a block is created, the concerned miner needs to solve a special logic puzzle before the block can be accepted for addition to the ledger. This puzzle is a cryptographic problem that requires time as well as computational skills to be solved. The first miner to solve this is given the miner’s fees. Also, as the puzzle is computationally very heavy, it ensures that only people with very powerful computer systems can even attempt to create a fraudulent block (as we shall see later, even if they are able to somehow solve the puzzle, there are other hurdles that they must overcome before their block gets accepted by the system).

*	Problems with Proof of Work
While the features of the proof of work algorithm managed to solve the issues mentioned above, these very features brought with them a major problem. The proof of work algorithm is intentionally made computationally heavy, but this also means that miners need to spend a huge amount of computational power for mining. This is harmful to the environment, and thus can’t be accepted as a long-term solution. Also, the need for large computational power motivates miners to start congregating into miner pools, where they use their combined power to mine and then they split the benefits. However, such monopoly of a single group over the network presents a security risk, and therefore isn’t favoured. For these reasons, alternatives to proof of work are now being strongly considered. 

*	Alternatives to Proof of Work
One popular alternative is proof of stake, currently the strongest contender to replace proof of work. In this, miners don’t compete for blocks. Instead, each miner stakes some very high amount of cryptocurrency as collateral. Based on the amount deposited and some other factors, an algorithm picks a certain miner for the task. He can then mine the block with no competition. If a miner is caught performing any malicious activity, his collateral is seized and he is banned from the system. Thus, miners are given incentive to remain honest. As there is no fixed miner’s fee for creating a block, each transaction has a transaction fee attached to it, directed to the concerned miner. A clear display of the growing popularity of proof of stake is that even Ethereum, one of the largest Blockchain based companies in the world, is migrating from proof of work to proof of stake.
Another famous alternative is proof of capacity, although it’s only slightly better than proof of work. Here, instead of paying with computational power, the miner pays with storage space. The algorithm stores plots of large data sets on the miner’s hard disk. More the plots, higher the miner’s chances of finding the next block to be mined.

*	Hashing
We now take a quick diversion to understand a concept called hashing which is vital to the smooth functioning of Blockchain. Hashing involves taking an input of any length (could be a string of characters, a transaction, or even an entire block) and producing a string of fixed length as output. A good hashing function is deterministic i.e., a given input produces the same output no matter how many times the function is run on it. In other words, if two hashes are different, it can be safely said that their original inputs were different too. Also, for a good hashing function, no two inputs produce the same output (or rather, the chances are astronomical). These two properties of hashing play a vital role in the functioning of Blockchain.

*	Merkle trees
Now that we have understood hashing, we can look at how transactions are stored within the block. If we were to simply store all transactions together, searching for a particular transaction would become tedious. Also, very often we don’t need to check the contents of individual transactions, but simply need to ensure that their overall integrity is preserved. This task is achieved using Merkle Trees.
A Merkle Tree is a binary tree (every node has at most two children) in which the leaf nodes are the hashes of the individual transactions, and every parent node is a hash of its two child nodes. If there aren’t enough transactions to satisfy all the leaves, they can simply be replicated, as transaction integrity is our main objective. By performing this hashing up the levels of the tree, we end up with a single hash at the root, known as Root Hash. Based on the explanation of hashing, we now know that if even a single transaction is altered, its hash changes, and this change travels up the tree, changing the root hash as well. Thus, each block uses a Merkle tree and stores the resultant transaction root hash to help maintain transaction integrity.

*	Immutability of the Blockchain
Once a miner creates a block, before he calculates the proof of work, he performs one last task. He takes the hash of the current latest block in the Blockchain and places it in the newly created block. Now, he calculates the proof of work and adds the new block. In this way, the various blocks are linked or chained together by their resultant hashes. This is why the technology came to be called Blockchain. 
Now, we’re finally ready to understand how the effect of immutability is achieved in Blockchain. If anyone tries to re-write even a single transaction within any block, the resultant hash of that block changes (recall the properties of a good hashing function mentioned earlier). Thus, that block’s hash no longer matches with the hash stored in its succeeding block. To cover up, the attacker would have to calculate a new proof of work for the manipulated block, then insert its new hash into the succeeding block. However, the moment he does this, the succeeding block’s resultant hash changes, producing the same problem again. Thus, in effect, to alter even a single transaction, the attacker would effectively have to re-calculate the proofs of work for all succeeding blocks within the Blockchain. Technically, this would be easier for a newer block (fewer successors) and tougher for an older block (more successors). However, on the whole, the task is more or less computationally infeasible. With this, we have achieved the effect of immutability within the Blockchain.

*	Consensus Within the Blockchain
We’re now ready to tackle the final property of Blockchains, consensus. Once a miner fully creates a block and preps it for addition to the chain, they broadcast it to the rest of the network. Each user picks this up and updates his/her copy of the Blockchain. However, in practical working, two miners working at different speeds may simultaneously produce blocks that have clashing transactions. More importantly, what if a malicious miner with sufficient computational power was to broadcast a fraudulent block? In this case, a user might receive multiple chains (or chain extensions). How would the user have any way of knowing which chain to accept?
This is where a system of consensus is needed i.e., a way for members of the system to agree on which chain to accept as the legitimate one. This is achieved by the working rule - The chain to be trusted is the one that has had the most computational work put into it.
Thus, each user accepts or works with the chain that is of maximum length. This is based on the assumption that at any point, no more than 50% of the mining pool of the system is malicious. Thus, it’s assumed that majority of miners are honest, and so they produce legitimate blocks faster than the malicious miners can produce fraudulent ones. This means that the legitimate chain will always be longer, and based on the consensus rule, this is the one that all users accept. As a result, the Blockchain has achieved consensus.
An important factor to be noted is that the consensus rule works on the assumption that more than 50% of the mining pool will never be malicious. If, however this were to happen, they could easily add fraudulent blocks to the chain. This is known as the 51% attack, and was highlighted by Satoshi in his original paper.

*	Conclusions
We have so far discussed all the basic features of Blockchain, and examined its internal implementation, at least at a theoretical level. On the technical side, there are several processes and intricacies not explored here. These are however, vital in tying the system together and allowing it to function as a comprehensive unit. 
In conclusion, Blockchain is definitely a newer field compared to other notable ones, but is in no way less impactful. Its effects are resonating throughout the world, and large-scale attempts are being made to utilize it to make advancements in several technologies. Concepts within Blockchain like Smart Contracts are quickly expanding its usability and functionality. Be it for faster file sharing through IPFS to help usher in Web 3.0, or in Linux Foundation’s Hyperledger Project to change the way we do business world over, the potential for Blockchain to change our lives is limitless and unquestionable. This is what makes it a subject of interest to computer scientists worldwide.

*NOTE*: This article mainly aimed to educate the reader on the basic features of Blockchain. Readers interested in delving further may refer to topics such as Smart Contracts, which greatly expand the functionality of the Blockchain.
Also, the concept of Blockchain was tackled here mainly from the viewpoint of Bitcoin specifically. There are other cryptocurrencies with different features that aim to solve some of Bitcoin’s perceived shortcomings. Outside of cryptocurrencies as well, there are other applications of Blockchain that are more dynamic, and with more diverse features, such as Ethereum and Hyperledger, to name a few.

