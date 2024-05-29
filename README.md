# Projects
## Trader
[https://github.com/bananna1/trader.git](https://github.com/bananna1/trader.git)

#### Contributors
Anna Giacomello
#### Languages
Rust
#### Description
Trader implements a BOT that is capable of exchanging currencies with three stock markets, implemented ad-hoc for this project. The markets have been developed by other contributors, not the author of this repository.\
The trader focuses on accumulating as many goods as possible, each time pondering what actions is better: whether to sell or buy, which currency to focus on, which market to focus on.

## HouseLocker
[https://github.com/davipase/HouseLocker.git](https://github.com/davipase/HouseLocker.git)\
[Link to report](assets/reports/report_houselocker.pdf)
#### Contributors
William Riccardo Duro, Anna Giacomello, Davide Pasetto, Federico Valbusa
#### Languages
Solidity, JavaScript
#### Description
HouseLocker is a project that aims to address a significant problem in the housing market for university students: too many room reservations are unofficial and solely based on trust, often happening via platforms that are not suitable for this kind of business, e.g. Facebook. This can lead to students being robbed or scammed by landlords, who usually have the upper hand in this kind of relationship.\
The solution implemented uses blockchain to create a platform that allows landlords and students to interact without having to rely on human trust.\
The business relationship is managed by a smart contract, which stores deposits temporarily, only releasing them to the respective parties when both parties are satisfied. Both parties are allowed to hibernate the contract at any moment if they feel something suspicious is going on. This allows for human intervention when deemed necessary, particularly by authorities in case of illegitimate actions performed by one of the parties.

The project includes a zero-knowledge proof mechanism implemented during user registration to verify that the registering entity is indeed the owner of the claimed address. Additionally, if the entity is a student, an additional zero-knowledge proof is conducted to confirm their student status using information sourced from universities, all without compromising privacy. This is necessary as the platform is exclusively available for student tenants.

## ASA - Dunder Mifflin
[https://github.com/bananna1/ASA_dunder_mifflin.git](https://github.com/bananna1/ASA_dunder_mifflin.git)\
[Link to report](assets/reports/report_asa.pdf)
#### Contributors
Anna Giacomello, Davide Pasetto
#### Languages
JavaScript, PDDL
#### Description
This project implements an autonomous software agent's behavior in a map. The purpose of the agent is to retrieve parcels, which have a limited lifetime, and deposit them in certain blocks of the map to obtain points and increment its own score.\
The project aims at refining the behavior of a single agent in order for it to maximize it score, and then at implementing cooperation mechanisms to collaborate with other agents.
The agent’s decision-making process follows a cyclical workflow: The _sensingLoop_ function is called periodically, and it generates a list of options based on the agent’s observations about the environment surrounding it. The options are filtered based on their utility, which is a custom value based on some calcula-
tions, and the best option is selected for execution. The selected option is added to the intention queue, managed by the _IntentionRevisionQueue_ class. _IntentionRevisionQueue_ continuously revises and executes intentions from the queue, ensuring that the most recent intentions are considered. Each intention is achieved by selecting and executing appropriate plans from the plan library.

Plan execution involves carrying out sub-intentions and performing actions to achieve the desired outcome. The process repeats, allowing the agent to adapt
its intentions and actions based on the changing environment. The choice of the queueing method for the Agent represent the choice of making most of the controls over the validity and the goodness of an Intention inside the sensingLoop function. It was opted for this implementative option because the execution and revision of Intentions inside the Agent class is done in an asynchronous function, and whilst this allows for a responsive change of Intention based on the surrounding environment, it also caused consistency problems when called several times a second. Therefore it was found a more sequential approach to yield the best result.

## Project DS
[https://github.com/bananna1/Project_DS_Giacomello_Vecellio.git](https://github.com/bananna1/Project_DS_Giacomello_Vecellio.git)\
[Link to report](assets/reports/report_ds.pdf)
#### Contributors
Anna Giacomello, Martina Vecellio Reane
#### Languages
Java
#### Description
This project is an implementation of a DHT-based peer-to-peer key-value storage service inspired by Amazon Dynamo. The system consists of multiple storage nodes
The partitioning is based on the keys that are associated with both the stored items and the nodes; the keys form a circular space or “ring”, i.e., the largest key value wraps around to the smallest key value. A data item with key K should be stored by the first N nodes in the clockwise direction from K on the ring, where N is a system parameter that defines the degree of replication.\
To implement replication, the system relies on quorums. Versions are associated internally with every data item to support consistent reads. System-wide parameters are present to specify the write and read quorums.\
A client can either ask to write or read items to any node in the system; the queried node is then responsible of forwarding the request to the ring.

Moreover, nodes can also:\
• **Join:** a node can join the ring; it relies on another node, called _bootstrapping peer_, to receive information about the ring. Then, the joining node issues requests to the nodes in the ring to receive the items it is going to be responsible for.\
• **Leave:** a node can be requested to leave the network. To do so, the leaving node announces its departure to the others and passes its data items to the nodes that become responsible for them after its departure.\
• **Crash:** a node has not left, it is just considered temporarily unavailable.\
• **Recovery:** when a crashed node is started again, instead of performing the join operation it requests the current set of nodes from a node specified in the recovery request.\
It should discard those items that are no longer under its responsibility (due to other nodes joining while it was down) and obtain the items that are now under its responsibility (due to nodes leaving).

## SSSSSS
[https://gitlab.com/smaniottonicola/ssssss.git](https://gitlab.com/smaniottonicola/ssssss.git)\
[Link to report](assets/reports/report_ssssss.pdf)
#### Contributors
William Riccardo Duro, Anna Giacomello, Nicola Smaniotto
#### Languages
Java
#### Description
SSSSSS - Shamir's Secret Sharing Secure Storage System is an implementation of Shamir's Secret Sharing to achieve security of files storage. It is of course based on the generation of shares that disclose a secret when a party possesses at least an amount of them equal to a threshold, which is set in the initialization phase.\
The functionalities a user can benefit from thanks to this project are the following:\
• Encrypt a file, to protect it from an attacker, with AES-256 GCM\
• Copy the encrypted file on all their devices, to have it always accessible\
• Set a threshold of devices that are needed to recover the file\
• New devices can be added later, from anywhere\
• Outdated or compromised shares can be excluded from the system\

## GearUp
#### Contributors
Anna Giacomello
#### Languages
Python
#### Description
GearUp is a service-oriented application that targets people wanting to starting their hiking hobby. It is an application that offers several functionalities:\
• Search for mountain huts\
• Find the paths to the huts, considering a chosen starting point\
• Get recommendations for gear

The gear recommendations are computed based on certain parameters given by the hike, such as altitude, length of the hike and weather conditions. The items recommended are beginner-friendly (they are all from Decathlon), with a price that ranges with respect to the quality required by the hike.

Note: the project is still under developing.
