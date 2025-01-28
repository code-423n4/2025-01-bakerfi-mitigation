# BakerFi Mitigation Review
- Total Prize Pool: $5,000 in USDC
  - HM awards: $4,000 in USDC
  - Judge awards: $1,000 in USDC
- [Warden guidelines for C4 mitigation reviews](https://code4rena.notion.site/Guidelines-for-C4-mitigation-reviews-ed10fc5cfbf640bd8dcec66f38b343c4)
- Starts January 28, 2025 20:00 UTC 
- Ends February 04, 2025 20:00 UTC 

## Important note 

Each warden must submit a mitigation review for *every* individual PR listed in the `Scope` section below. **Incomplete mitigation reviews will not be eligible for awards.**

## Findings being mitigated

Mitigations of all High and Medium issues will be considered in-scope and are listed here:

- [F-1: Users may encounter losses on assets deposited through `StrategySupplyERC4626`](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-1)
- [F-2: Anyone can call StrategySupplyBase.harvest, allowing users to avoid paying performance fees on interest](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-2)
- [F-6: _deployedAmount not updated on StrategySupplyBase.undeploy, preventing performance fees from being collected](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-6)
- [F-13: There are multiple issues with the decimal conversions between the vault and the strategy ](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-13)
- [F-17: Transactions that use .permit can be front-run to grief the user and steal his funds](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-17)
- [F-18: Malicious actors can exploit user-approved allowances on `VaultRouter` to drain their ERC20 tokens](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-18)
- [F-19: Malicious actors can exploit user-approved allowances on `VaultRouter` to drain their ERC4626 tokens](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-19)
- [F-3: VaultBase is not ERC4626 compliant](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-3)
- [F-4: New strategy can not work due to insufficient allowance](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-4)
- [F-5: `MultiStrategy#removeStrategy()` cannot remove leverage strategies that still have deployed assets ](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-5)
- [F-12: Even when the Vault contract is paused, the rebalance function is not paused ](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-12)
- [F-16: `_maxDeposit` check is incorrect](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-16)
- [F-26: The `dispatch` function of the `VaultRouter`, does not work as intended, with PULL_TOKEN action](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-26)
- [F-27: Incorrect whitelist validation in VaultBase.sol](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-27)
- [F-33: The withdrawal of Multi strategies vault could be DoSed while asset deposits remain unaffected](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-33)
- [F-34: The calculation of `assetsMax` is incorrect](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-34)
- [F-36: The Vault Manager is unable to delete the last strategy from `MultiStrategyVault`](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-36)
- [F-37: The `StrategySupplyMorpho` allow to use wrong token in `_asset`](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-37)
- [F-43: StrategySupplyBase.undeploy does not return the amount of assets actually undeployed, which can cause a withdrawal to fail](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-43)
- [F-40: VaultRouter cannot be used for deposits when it reaches the maximum deposit limit](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-40)


## Scope

### Branch

https://github.com/baker-fi/bakerfi-contracts/tree/develop


### Mitigation of High & Medium Severity Issues

| URL | Mitigation of | 
| ----------- | ------------- |
| https://github.com/baker-fi/bakerfi-contracts/pull/17 | F-1 |
| https://github.com/baker-fi/bakerfi-contracts/pull/15 | F-2 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/12 | F-6 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/24 | F-13 | 
| https://github.com/baker-fi/bakerfi-contracts/pull/23 | F-17 | 
| https://github.com/baker-fi/bakerfi-contracts/pull/20 | F-18 | 
| https://github.com/baker-fi/bakerfi-contracts/pull/19 | F-19 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/27 | F-3 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/13 | F-4 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/16 | F-5 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/3 | F-12 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/4 | F-16 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/11 | F-26 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/26 | F-27 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/5 | F-33 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/22 | F-34 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/18 | F-36 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/6 | F-37 | 
| https://github.com/baker-fi/bakerfi-contracts/pull/28 | F-43 |  
| https://github.com/baker-fi/bakerfi-contracts/pull/4 | F-40 |  

## Out of Scope

All sponsor `acknowledged` (wontfix) findings, including:
- [F-8: Sending tokens to a Strategy when totalSupply is 0 can permanently make the Vault unavailable](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-8)
- [F-10: Permit doesn't work with DAI](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-10)
- [F-35: Cannot withdraw tokens from all strategies in MultiStrategyVault when one third party is paused](https://code4rena.com/evaluate/2024-12-bakerfi-invitational/findings/F-35)

All known issues listed in the preceding audit's [repo](https://github.com/code-423n4/2024-12-bakerfi?tab=readme-ov-file#automated-findings--publicly-known-issues) are considered known issues and out of scope. 
