# Loot tournament

This project is a tournament system for Loot NFT holders.

16 Loot warriors place ETH in the treasure chest, and proceed to fight each other in mortal combat until only one prevails.

Warriors are randomly placed in 1:1 matches and are eliminated from the tournament upon defeat.
The outcome of the 1:1 battle is determined by the rarity of the Loot NFT, a random factor, and additional rules on set combinations and synergistic NFTs to be determined at a later time.

1st place claims 40% of the treasure chest, 2nd place 20% and 3rd place 10%. The 13 remaining loot warriors claim 2% of the treasure chest as a gas reimbursement. 2% is reserved for the developer and another 2% for whoever paid the gas price for the match.

Loot holders can place funds on the smart contract as `signup(lootTokenId, totalEth, maxEthPerRound)`. Their submission stays active for indefinite tournaments until they withdraw from the contest. A separate smart contract call conducts the tournament by choosing 16 of the highest-paying contestants, rewarding the caller 2% of the prize pool. Each participant is deducted the same fixed participation fee based on the lowest `maxEthPerRound` across all participants

Tournaments should keep happening automatically by bots as long as the prize pool is at least 50x of the gas price of running a tournament. Assuming a .04 ETH gas price, the pool size would be 2 ETH.
