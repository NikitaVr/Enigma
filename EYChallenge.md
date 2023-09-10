## Requirement 0:

Project Info



* The project name and description of solution. 

    * Project Name: Enigma: Privacy Enabled Private Address Book

    * Description: 
        * The Problem is that crypto users often have to send their addresses and contact information to each other. This information is siloed, and currently, there is no interoperability between apps without using a completely public storage like ENS. A user might save a friend’s address in Metmask’s address book, but then that data is not available on other devices and apps. This leads to sending funds to wrong addresses and address poisoning attacks that steal user funds.
        * The Solution is Enigma: an encrypted on-chain address book. A user can choose who to share their details with, and keep the data accessible on chain, without revealing the actual contents of the addressbook
        * This enables Wallets and Dapps to display private address data to users, without leaking it to anyone else. Wallets can pull in the private data and decrypt it with the user’s private key.
        * The core benefit is that shared user contact information becomes interoperable across any app used, such as Wallets, Dapps, Exchanges, etc. Without revealing to anyone the contents of the encrypted address book.
        * Additionally, by using Nightfall private transactions, we can ensure that the social graph between users is also kept hidden and cannot be used by scraping and analytics companies against the user.




* Names of team members and contact info (email/github) 


    * Team: ChainPatrol
    * Nikita Varabei - nikita@chainpatrol.io -[ https://github.com/NikitaVr](https://github.com/NikitaVr)
    * Vito Giovannetti - Vito@chainpatrol.io -[ https://github.com/vgchainpatrol](https://github.com/vgchainpatrol)
    * William Stevens - william.evans.stevens@gmail.com - (GitHub N/A) 
    * Ayoola John - ayoola@astronaut.chat - [https://github.com/ayoola](https://github.com/ayoola) 



## Requirement 1:

Team must attend the EY Workshop: How to implement privacy for public blockchains



* Provide your team name, and a list of team members that attended the EY Workshop.
    * Team Name: 
        * ChainPatrol 

    * Members Attended Workshop
        * Nikita Varabei
        * Vito Giovannetti
        * William Stevens
        * Ayoola John  



## Requirement 2:

Solution must be designed to run on a public network.



* Our smart contracts will be deployed to Ethereum Mainnet using the Hardhat framework with configurable contract addresses.
* The frontend will be hosted on IPFS/Filecoin and interact with the public chain.
* Backend services will be containerized and run on AWS, interacting with public nodes.
* We will use Alchemy to connect to the Ethereum mainnet.
* The benefit of storing this data on a public network is that it enables any app to pull in the user’s address book and allow them to decrypt their contacts across any client.


## Requirement 3:

Solution must be designed to run under privacy (implementation optional).

Write one paragraph on why your solution will benefit from implementing privacy.



* Encrypting the data using the recipients public key and storing on a public blockchain can be enough to hide the sensitive contact details such as email and phone number, however this does still reveal the social graph between connected users. As we have seen with social networks, a lot of data can be revealed about an “anonymous” user by only looking through their social graph and inferring data from their friends and connections. An additional level of privacy is needed to hide the user’s social graph so that they can share their sensitive contact information and benefit from interoperability without leaking their social graph. 


Write one paragraph on which privacy solution you selected (and why).



* We selected Nightfall protocol as the privacy solution:
* Nightfall enables users to share the address book with each other and making the data available on chain to any app to integrated, without revealing the users’s social graph. This is useful as it allows users to privately share sensitive contact information with other users they trust, while keeping this data hidden from other users and keeping their social graph hidden from analytics and tracking tools. 


Create an Architecture diagram on how your solution will bridge between the public network and a privacy solution (ie: Nightfall). What services & connections will you use? What data/tokens will be shared or transferred between networks? What workflow(s) will be used under privacy?



* User contact information is encrypted and stored on a public Ethereum Mainnet.
* Where to lookup the data is sent to User B through a token on nightfall
* The Shield smart contract holds private token commitments and verifies zkSNARK proofs.
* Whisper is used for encrypted messaging between parties.

![diagram 1](./Screen%20Shot%202023-09-10%20at%2012.09.13%20PM.png)

![diagram 1](./Screen%20Shot%202023-09-10%20at%2012.08.42%20PM.png)

![diagram 1](./Screen%20Shot%202023-09-10%20at%2012.09.08%20PM.png)



