# LRT-Integration-Docs
Documentation about integrating GammaSwap with Liquid Restaking Tokens

Note: Examples given are with wstETH and USDC but any combination of tokens can be used.

### Two types of integrations:
1. Providing liquidity: Reward unborrowed tokens with LRT points, earn interest on borrowed tokens
2. Borrowing liquidity: Reward borrowed tokens with LRT points, pay interest to liquidity providers

## 1. Providing liquidity (LRT token and some other token)
  
Providing liquidity into a full range x*y=k AMM. Users would earn points from the LRT token in the AMM.

Example:

user1 provides 100 wstETH and 100 USDC as liquidity into the AMM. His wstETH balance is 100 wstETH. Total wstETH in the platform is 100 wstETH.

## 2. Borrowing liquidity

Borrowing liquidity from the above mentioned AMM in order to turn impermanent loss into impermanent gain. Users would earn points on wstETH held as collateral against the AMM liquidity loan.

Example:

After user1 above provides liquidity, user2 borrows 90 wstETH and 90 USDC from the AMM as a liquidity loan, holding 90wstETH and 90 USDC as collateral. User2 wstETH balance is 90 wstETH. 

However, user1’s balance has now changed to 10 wstETH because user2 borrowed 90 wstETH from it. Total wstETH in the platform is still 100 wstETH because wstETH never leaves the platform. All loans are held inside the GammaSwap platform (either the AMM as liquidity or in the GammaPool as collateral for a loan). User1 of course would be compensated in interest payments from user2 for lending his wstETH which he can use to earn LRT point rewards.

