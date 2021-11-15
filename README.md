# Liminal.market
Liminal is a platform for buying securities (stock, bonds, commodities, etc.). It allows users to use their crypto currency to buy securities without converting the crypto to a localized fiat currency and finding a broker to facilitate the trade. The trade is recorded as tokenized security to the blockchain as ERC20 smart contract, allowing for transparency & accountability. All done through a simple user interface or through programmable smart contracts. 

# Empty repository
For now this is an empty repository for LINK Midway Check-in

# LINK Hackathon Fall 2021
This project is entering into LINK Hackathon Fall 2021. It is using LINK and Moralis to run the system as long with other 3rd party services. At current development only 1 table with 2 columns are needed to run the system, everything else is stored on the blockchain. We hope to get this down to zero. Code is written in Solidity and being tested on one of the Ethereum test networks, but with Moralis we aim to launch any of the low gas cost EVM networks.

# Why trade securities using Liminal?
Liminal allows you to have all your security trades recorded on the blockchain & owning the underlying security at the same time. This has some legalatory benefits. Adding off-chain data to the blockchain adds transparency & accountability benefits. 

# Website (www.liminal.market)
The website https://www.liminal.market/ will be the entry point for users to buy and sell. First step is Authorization.

## Authorization
User is authorized using his wallet. To have access to the system, the user logs in with his wallet by signing a message. This gives cryptographic certainty that the user is who he says he is. Good bye username and passwords. Next is Authentication.
## Authentication
Before any order can be made in the system, the user needs to authenticate using KYC or other authentication process acceptable by the market that will be traded in. Liminal will implement this authentication through a 3rd party solution. Now that he has been authenticated, he can create orders.
## Orders (buy/sell)
Buying and selling securities will be a simple interface where the user selects the security and the amount he wants to buy. It could be something similar to Uniswap. Features such as slippage, stop price and other settings are also an option.
### Buy
When buying a security, the following process happens.

- User selects to buy $100 worth of Apple stock (AAPL)
- Liminal requests access to users wallet to withdraw $100
- User accepts
- 1st transaction (on the blockchain)
  - Liminal moves $100 from user wallet to Liminal smart contract
  - Liminal removes fee for transaction
  - Liminal sends money to bank account of broker - this is issue
- Liminal executes order by sending it to broker API
- Order has been executed by broker
- 2nd transaction
  - Liminal receives notification that order has been executed
  - Liminal writes to blockchain that this wallet owns $100 worth of AAPL stock as a token. 
  - Current AAPL price is $154, so user gets 0.66015 shares Ef það ætti að trade'a securities þá ætti að gera það svona...

The wallet should show the result

![image](https://user-images.githubusercontent.com/103004/141854224-2af4a9bb-a4ac-4be1-b57f-5f95f7443353.png)

### Sell
When selling a security, the following process happens
- User selects to sell $100 worth of AAPL token
- User signs message to confirm execution using his wallet
- 1st transaction (on the blockchain)
  - AAPL token sent to Liminal smart contract
  - Liminal removes fee
  - Liminal sends sell order to broker api
  - Order has been executed by broker
- 2nd transaction
  - Liminal receives notification that order has been executed
  - Liminal burns AAPL token that was moved to contract
  - Liminal write to blockchain value stored at the broker on a token
  - Liminal sends token to user

Because of cost & speed in the off-chain world, it would be wise to simply keep the money in the broker account for the next trade. If the user wants his money, he would then execute that separately as it can take days and high cost.

## Basic flow of order
![image](https://user-images.githubusercontent.com/103004/141854119-aa6f0d9f-c17f-451e-aa6d-ee506f2da511.png)

# Revenue
Revenue income for Liminal should be simple to understand. Simplest version is a fee structure on buy and sell. 
- Fee structure on buy and sell
- Fee is removed at transaction time
- Should start around 0.5% and then aim to lower it with time
  - $1 million throughput would give $5.000 in fee

# Opportunities
## Diversifying your portfolio
Liminal will allow users that have fully moved their investment to the crypto space to diversify their portfolio to other things, not only holding value in crypto currency but also in securities registered on stock markets.
## Move users to blockchain
People & companies that have investments both in securities as well as in crypto currencies can now fully move everything to the blockchain. This will lower their cost, increase transparency, lower financial oversight
## Funds
Some funds(such as pension funds) are limited by law on what they can trade on and how much in each category. Using Liminal, funds can fully run on a blockchain and are not limited to what they can buy in. This would give full transparency as well and allow for full DAO funds (video).
## Funds created by users
With blockchain technology, the opportunity to run funds managed by rules and computers has become a reality. SetProtocol is a good example of this. Users can set up a fund that other people can join. Since Liminal has an open smart contract, external protocols(e.g. SetProtocol) can use Liminal to execute orders.
## Lego smart contracts
Since Liminal smart contract is open to everybody, any programmer can build on top of it. This can allow other services to implement a trading feature with the stock market and take their own fees. 
## Swap
User should be able to swap tokenized securities as long as the recieving user is KYC verified
## Staking
Although currently institutions are not supported (KYB) in first version, it should be possible to allow staking when institutions are supported

# Potentials
## First to market
Currently there is no service providing this in the blockchain world. Being first to market and having an open access to the contract allowing for other contracts and services to build on, give the opportunity in the long term to be the underlying component of multiple services. 

This way, other services will get people to use Liminal without them even knowing it. This is the case with services like Uniswap, as a service that was first to market, people started to use them in their smart contracts.
## Improved experience
It will become easier and easier to use Liminal with time. Most difficult part is registration for KYC. KYC wizard will not be needed in the future to register as the KYC will be stored on the blockchain and Liminal will only need one click to retrieve it.

Moving money to the broker will become easier with time. The end goal should be to move the money using blockchain to the broker's account.

With these two changes that will come; UX will improve, cost will go down and speed for trades will go down to a few seconds.
## Funds
Funds have a lot of money to manage and this is a source of potential revenue to tap into. The goal should be to introduce this new technology and what the consequences are to the funds market. With full autonomy, funds can be runned at an extremely low cost. In current landscape funds are taking from 0.5% and up to 3.5% commission. With this technology it could be taken down considerably, into the permille(‰). Like with any business, a possible 10x lower price for the customer, full transparency, accountability and the security that the blockchain provides, should give a big advantage to the first players that adopt this technology. 

# Financial Regulations for Liminal
Liminal is simply the software that you use to execute a trade and blockchain is the database. 

Two critical items should ALWAYS be followed
- It should ALWAYS be possible to prove to 100% certainty what Liminal cannot take or misuse money from the user.
- Liminal should NEVER put customers money into its bank account or other account that might need financial oversight.

Liminal should not need (or very minimal) interference from regulatory institutions. The software runs on the blockchain, can be viewed and verified. This way you can be sure what it does and it never changes. 

# DAO
Long term goal WILL be to turn Liminal into a DAO. This gives a few things that allow Liminal to grow the most.

Setting Liminal up as DAO will give legitimacy to the project. 
It will be runned by the community giving transparency and accountability to token holders
This gives liquidity to shareholders of Liminal
DAO members will have voting rights and get dividend from holding the token

To have trust, the smart contracts must be open and validated. Having them open means everybody can copy it and set up their own LiminalCopy smart contract. LiminalCopy can then set up a DAO allowing its users to make decisions on what the direction of the DAO should be.

This brings up the decision making for people wanting to implement trading securities in their smart contract

If I'm creating a new service that needs to buy securities, should I use Liminal or LiminalCopy to execute orders in my smart contract. LiminalCopy DAO would most likely win as it's transparent and by buying tokens, I can influence the direction it should go. This is why it is inevitable to set up Liminal as DAO.

# Off-chain operations
Since current stock markets don't run on blockchain technology, part of the transaction needs to be executed off-chain. The part where API calls are made to a broker to execute an order is executed off-chain. As soon as an order has been executed by the broker, Liminal writes that information to the blockchain.

Off-chain activity cannot be verified with 100% certainty but is runned by licensed companies with oversight from governmental entities.
# Source of truth
The question of the source of truth in a system with 2 databases always comes up. Our 2 databases are the Broker(Stock exchange) and blockchain. In this case the Broker is always the source of truth and the blockchain is mirrored by it.  In case of breach of the smart contract your securities would be safe and the smart contract would be rebuilt using the brokers database as current point in time.
