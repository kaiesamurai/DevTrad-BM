# DevTrad: A Zero-Knowledge Proof Trading Simulation Game

## What is DevTrad
DevTrad is a simulation game that replicates real-world commodity trading. Utilizing zero-knowledge proof technology, players can demonstrate the authenticity and security of their transaction results without revealing their proprietary trading strategies.

## Inspiration
In real market transactions, each trader or quantitative institution has unique trading strategies that determine their success. To prevent these strategies from becoming ineffective, traders need to keep them confidential. DevTrad addresses this by allowing players to prove their profitability without disclosing their specific trading moves, using zero-knowledge proofs.

### Example: Alice and Bob
Alice and Bob, friends who enjoy trading games, are used to evaluating Bob's trading skills. Bob, an experienced trader, wants to prove his ability without revealing his strategies. Alice uses a controlled computer to verify Bob's trading outcomes by comparing account balances before and after transactions, ensuring Bob’s strategy remains confidential. This setup is mirrored in DevTrad, where the transparency of blockchain allows validation of trading skills without exposing the strategies themselves.

## How to Play

### Main Scene
1. Click the "Start Game" button on the main interface and pay the $2 registration fee to join the game.
2. Click the "Rank List" button to view the current scores of top players.

### Game Scene
1. Players can check market news to understand commodity price fluctuations.
2. The transaction page displays personal information such as cash, total assets, transaction progress, and maximum positions.
3. Expand maximum positions by paying $10 in ETH or 50% of the current total assets in cash.
4. The list on the left shows currently tradable products with details like name, price fluctuation range, and current price.
5. Purchase items based on your cash situation and manage positions shown on the right, which display average purchase prices and quantities.
6. After completing transactions, click "Next Year" to verify transactions and generate a zero-knowledge proof.
7. Click "End Game" to finalize the player's transaction results through a smart contract, saving the total asset amount after transactions.

The smart contract interactions only involve the final score and zero-knowledge proof, without requiring specific transaction details. Once the collected fees reach a certain threshold, rewards are distributed to the top players of the season.

## How We Built It

### Logo and Assets
The game logo and most assets were created using Photoshop.

### Nori
Nori is a powerful domain-specific language for SNARK proving systems. We used Nori to write a zero-knowledge proof circuit for verifying transaction correctness in the game.

### Sindri
Sindri is a ZK Developer Cloud that provides the infrastructure needed for developing, deploying, and scaling zero-knowledge proofs. We used Sindri to generate proofs quickly, meeting the high concurrency demands of our game.

### Chainlink Data Feeds
Chainlink Data Feeds connect our smart contracts to real-world data such as asset prices. We used AggregatorV3Interface to get the latest prices of BTC, ETH, and USDT, saving them to the player's on-chain data and controlling market simulation data in the game. The calUsdToEthAmount method estimates the amount of ETH required to pay specific amounts in USD, ensuring accurate transactions for game entry fees and position expansions.

### Scroll Sepolia Testnet
Verified smart contracts:
- GAME_CONTRACT_ADDRESS: 0x252CB7801c9793e9607ACFcE4253547b993026bA
- VERIFY_CONTRACT_ADDRESS: 0x497B05AC1F135B390d5Ac0c2dDb06C5a915Af46F

## Challenges We Ran Into
- Ensuring confidentiality of trading strategies while proving transaction authenticity.
- Integrating zero-knowledge proofs seamlessly with high-frequency trading.

## Accomplishments That We're Proud Of
- Successfully using zero-knowledge proofs to maintain strategy confidentiality.
- Creating a user-friendly simulation that accurately reflects real-world trading.

## What We Learned
- The importance of confidentiality in trading strategies.
- Effective integration of zero-knowledge proofs with blockchain technology.
## Inspiration
The inspiration for DevTrad came from the need to keep trading strategies confidential while demonstrating their effectiveness. In real market transactions, the secrecy of a trading strategy is crucial for maintaining its success. DevTrad leverages zero-knowledge proof technology to allow traders to prove their profitability without exposing their strategies.

## What it does
DevTrad is a simulation game that allows players to engage in commodity trading. It uses zero-knowledge proofs to verify the authenticity and profitability of transactions without revealing the underlying trading strategies. Players can demonstrate their trading skills, validate their success, and compete with others while keeping their proprietary methods secure.

## How we built it
DevTrad was built using several key technologies:
- **Photoshop** for designing the game logo and assets.
- **Nori**, a domain-specific language for SNARK proving systems, to write zero-knowledge proof circuits.
- **Sindri**, a ZK Developer Cloud, to run zero-knowledge proof circuits and generate proofs efficiently.
- **Chainlink Data Feeds** to connect smart contracts to real-world data, such as asset prices, ensuring accurate and up-to-date market simulations.
- **Scroll Sepolia Testnet** for deploying and verifying smart contracts.

## Challenges we ran into
- Ensuring the confidentiality of trading strategies while providing verifiable proof of transaction authenticity.
- Integrating zero-knowledge proofs in a way that supports high-frequency trading.
- Balancing the need for security with the user-friendly design of the game.

## Accomplishments that we're proud of
- Successfully creating a simulation game that maintains strategy confidentiality through zero-knowledge proofs.
- Developing a user-friendly interface that accurately simulates real-world trading.
- Efficiently generating zero-knowledge proofs with Sindri to handle the high concurrency demands of the game.

## What we learned
- The critical importance of confidentiality in trading strategies.
- Effective integration and application of zero-knowledge proofs with blockchain technology.
- How to design a secure yet user-friendly trading simulation game.

## What's Next for DevTrad
- Expanding support for additional commodities and trading features.
- Continuously improving the user interface based on player feedback.
- Enhancing security features to protect user data and assets.
- Exploring partnerships to integrate more financial services and tools within the game.
