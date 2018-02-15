# Comparison of consensus algorithm

This article is organized by playjokes in the learning process. If there is any mistake, please correct me.

## Background

Virtual currency based on blockchain, such as bitcoin(is essentially a distributed database), is a distributed accounting system. But the difference with distributed database is that the nodes of distributed database trust and cooperate with each other, while the nodes in the block chain are mutual suspicion and mutual restriction. It must tolerate malicious node attacks and eventually make the system run unanimously. It's called the Byzantine error, the famous Byzantine general problem, the general version of the general problem. The key to the Byzantine general problem is that most generals are known to be loyal.

The Byzantine fault tolerance of the guarantee system is the main goal of designing a distributed accounting system. Now let's look at how various existing algorithms work to make the system withstanding malicious attacks.

## PoW（Proof of Work）

### Method

PoW is to find a random number X, when we add this X to the transaction information and calculate the block hash value, the result must be N leading 0. The difficulty of this problem can be adjusted by adjusting the number of the leading 0, the more the leading 0, the greater the amount of work. At present, the value is set in bitcoin to meet 10 minutes to confirm a transaction. It takes a lot of trial and error to get a block hash value, and the computing time depends on the machine's hashing speed. When a node provides a reasonable block hash value, it shows that the node has indeed undergone a lot of attempts to calculate. Of course, it can not get the absolute value of calculation times due to finding reasonable Hash is a probability event. When the node has the computing resource of the whole network n%, the node has the probability of n/100 to find the target Hash. So when a hacker who wants to attack the network has 51% computing resource, then the system rate can be rewritten by some hackers. If the computation resource is enough, all the trading records can be denied to generate new chains.

### Scenario and Features 

The consensus algorithm using PoW in bitcoin requires all nodes to participate in the algorithm, which is limited by the speed of block propagation in the whole network and the limitation of 10 minutes. So its transactions are too slow and limited in performance.

## PoS（Proof of Stake）

## DPoS（Delegated Proof of Stake）

## PBFT（Practical Byzantine Fault Tolerance）