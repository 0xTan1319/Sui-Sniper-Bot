# Sui-Sniper-Bot
Sniper bot on sui blockchain

Certainly! Below is the finalized TypeScript code for your Sui blockchain sniper bot, incorporating the following configurations:

- Slippage: Set to 25%.
- Minimum Liquidity Amount: Set to 10,000 (10K).
- Buy Amount: Set to 50 SUI.
Additionally, I have provided a comprehensive step-by-step guide on how to set up, configure, and launch the bot.

## Contact

If you have a question, feel free contact here: [Telegram: @shiny0103](https://t.me/shiny0103)

## Setup .env file

### Create a .env File

Create a .env file in the project directory to store all sensitive information and configurations.

### Populate the .env File

Open the .env file and add the following configurations. Replace placeholder values with your actual credentials and desired settings.

```bash
# Private Key for Sui Wallet (Hex string without 0x prefix)
PRIVATE_KEY=your_private_key_here

# RPC Endpoint
RPC_URL=https://fullnode.devnet.sui.io

# Inside API Configuration
INSIDE_API_URL=https://api.inside.io/getContractScore
INSIDE_API_KEY=your_inside_api_key_here

# MovePump API Configuration
MOVEPUMP_API_URL=https://api.movepump.dex/getNewContracts
MOVEPUMP_API_KEY=your_movepump_api_key_here

# TweetScout API Configuration
TWEETSCOUT_API_URL=https://api.tweetscout.io/getTwitterScore
TWEETSCOUT_API_KEY=your_tweetscout_api_key_here

# Trading Score Thresholds
SCORE_THRESHOLD=80
TWITTER_SCORE_THRESHOLD=50

# Trading Parameters
SLIPPAGE=0.25             # 25% Slippage
MIN_LIQUIDITY=10000       # Minimum Liquidity of 10K
BUY_AMOUNT_SUI=50         # Buy Amount of 50 SUI
CHECK_INTERVAL=60000      # Check every 60,000 ms (60 seconds)

# DEX API Keys (if required)
BLUEMOVE_API_KEY=your_bluemove_api_key_here
CETUS_API_KEY=your_cetus_api_key_here
```

### Example Console Output:
```
Initializing Sniper Bot...

[Monitor] Starting monitoring for new contracts on MovePump...
Fetched 3 new contracts from MovePump.

[Process] Evaluating contract: 0xABC123...
Contract score for 0xABC123: 85
Twitter score for 0xABC123: 60
Bonding curve for 0xABC123 is 100%.
Liquidity for 0xABC123 meets the minimum requirement.
All checks passed for 0xABC123. Proceeding to snipe.

Attempting to execute trade on BlueMove for contract 0xABC123...
Trade executed successfully on BlueMove for contract 0xABC123

Attempting to execute trade on Cetus for contract 0xABC123...
Trade executed successfully on Cetus for contract 0xABC123

Attempting to execute trade on MovePump for contract 0xABC123...
Trade executed successfully on MovePump for contract 0xABC123

[Monitor] Starting monitoring for new contracts on MovePump...
No new contracts found at this time.
```


