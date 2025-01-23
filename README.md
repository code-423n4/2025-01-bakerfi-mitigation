# BakerFi Mitigation Review
- Total Prize Pool: 5,000
  - HM awards: XXX XXX
  - Judge awards: XXX XXX
- [Warden guidelines for C4 mitigation reviews](https://code4rena.notion.site/Guidelines-for-C4-mitigation-reviews-ed10fc5cfbf640bd8dcec66f38b343c4)
- Starts January 28, 2025 20:00 UTC 
- Ends February 04, 2025 20:00 UTC 

## Important note 

Each warden must submit a mitigation review for *every* individual PR listed in the `Scope` section below. **Incomplete mitigation reviews will not be eligible for awards.**

## Findings being mitigated

Mitigations of all High and Medium issues will be considered in-scope and listed here.

- [F-1: Users may encounter losses on assets deposited through `StrategySupplyERC4626`](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-1)
- [F-2: Anyone can call StrategySupplyBase.harvest, allowing users to avoid paying performance fees on interest](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-2)
- [F6: _deployedAmount not updated on StrategySupplyBase.undeploy, preventing performance fees from being collected](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-6)
- [F13: There are multiple issues with the decimal conversions between the vault and the strategy ](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-13)
- [F17: Transactions that use .permit can be front-run to grief the user and steal his funds](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-17)
- [F18: Malicious actors can exploit user-approved allowances on `VaultRouter` to drain their ERC20 tokens](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-18)
- [F19: Malicious actors can exploit user-approved allowances on `VaultRouter` to drain their ERC4626 tokens](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-19)
- [F3: VaultBase is not ERC4626 compliant](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-3)
- [F4: New strategy can not work due to insufficient allowance](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-4)
- [F5: `MultiStrategy#removeStrategy()` cannot remove leverage strategies that still have deployed assets ](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-5)
- [F12: Even when the Vault contract is paused, the rebalance function is not paused ](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-12)
- [F16: `_maxDeposit` check is incorrect](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-16)
- [F26: The `dispatch` function of the `VaultRouter`, does not work as intended, with PULL_TOKEN action](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-26)
- [F27: Incorrect whitelist validation in VaultBase.sol](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-27)
- [F33: The withdrawal of Multi strategies vault could be DoSed while asset deposits remain unaffected](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-33)
- [F34: The calculation of `assetsMax` is incorrect](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-34)
- [F36: The Vault Manager is unable to delete the last strategy from `MultiStrategyVault`](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-36)
- [F37: The `StrategySupplyMorpho` allow to use wrong token in `_asset`](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-37)
- [F43: StrategySupplyBase.undeploy does not return the amount of assets actually undeployed, which can cause a withdrawal to fail](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-43)
- [F11: The `_handleSweepTokens` function lacks the ability to withdraw native ETH](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-11)
- [F14: The interaction between the router and the ERC4626 vault lacks slippage control](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-14)
- [F30: Strategies cannot be rebalanced correctly](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-30)
- [F31: VaultRouter cannot be used for deposits when it reaches the maximum deposit limit](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-31)



## Scope

### Branch

https://github.com/baker-fi/bakerfi-contracts/tree/develop


### Mitigation of High & Medium Severity Issues

| URL | Mitigation of | 
| ----------- | ------------- |
| https://github.com/baker-fi/bakerfi-contracts/pull/17 | F1 |
| https://github.com/baker-fi/bakerfi-contracts/pull/15 | F2 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/12 | F6 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/24 | F13 | 
| https://github.com/baker-fi/bakerfi-contracts/pull/23 | F17 | 
| https://github.com/baker-fi/bakerfi-contracts/pull/20 | F18 | 
| https://github.com/baker-fi/bakerfi-contracts/pull/19 | F19 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/27 | F3 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/13 | F4 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/16 | F5 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/3 | F12 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/4 | F16 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/11 | F26 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/26 | F27 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/5 | F33 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/22 | F34 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/18 | F36 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/6 | F37 | 
| https://github.com/baker-fi/bakerfi-contracts/pull/28 | F43 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/21 | F11 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/25 | F14 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/14 | F30 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/4 | F31 |  


### Additional scope to be reviewed

These are additional Low Severity changes that will be in scope.

| URL | Reference ID | 
| ----------- | ------------- |
| https://github.com/baker-fi/bakerfi-contracts/pull/21 | F11 | 
| https://github.com/baker-fi/bakerfi-contracts/pull/25 | F14 | 
| https://github.com/baker-fi/bakerfi-contracts/pull/14 | F30 | 
| https://github.com/baker-fi/bakerfi-contracts/pull/4  | F31 | 
 

## Out of Scope

N/A
