![gitvern logo](https://github.com/gitvern/media/raw/master/logo/logo-text-bg.png)

## DAO Governance based on Github

Enabling easy to implement and use DAO Governance for Open Source development projects, using a governance token in any EVM chain for cost effectiveness.

### System Components:

- [x] [GitHub](#github)
- [ ] [DAO Repository](#dao-repository)
- [ ] [Smart-Contracts](#smart-contracts)
- [ ] [Dashboard](#dashboard)
- [ ] [GitHub App](#github-app)

#### GitHub:

- GitHub is the most important piece of this system, as it will serve as contributor interface to most of the activities
- It is suggested to create a GitHub Organization and also the main projects that the DAO will manage, like: Development, Marketing, Social Media, etc
- Then organize the issues (work) under those projects
- We will also install our GitHub App on this Organization, so that we can verify and execute on-chain transactions when some activities take place, and also store off-chain data in GitHub issue comments for future reference and transparency
- 

#### DAO Repository:

- You can find a template DAO Repository [here](https://github.com/gitvern/dao), using gitvern project as an example
- Main DAO public configuration goes here, as it can be accessible from both GitHub App and the Dashboard, e.g., token info, treasury contract, contributor profiles, leader profiles, issue weight payouts, etc
- All this configuration is subject to be agreed in leader meetings, and token holders consulted in an issue if needed
- Also daily administrative activity of the DAO should have it's place here, for instance, meeting minutes, budget approvals, etc
- 

#### Smart-Contracts

- Set of smart-contracts to be used as a reference, when deploying each DAO Project's own contracts for:
    - Governance Token contracts
    - Pre-market Liquidity Building contracts using a UniSwap Liquidity Pool
    - Development Treasury contracts using DAO and LP tokens
- Governance Token contracts with transfer locking and ERC223 based to avoid getting stuck in contracts
- Pre-market Liquidity Building contracts serve as a means of gathering external liquidity to a DAO Governance Token, and simultaneously build up a DAO Treasury without "selling" tokens in an ICO - these contracts use a dutch auction system to derive a final base price for pre-market liquidity providers, enforcing a fair token distribution and price among all parties - then the token should become transferrable and the contract allows token holders to claim their LP tokens from the UniSwap Liquidity Pool, representing their pair of 50% ETH / 50% DAO Token
- Development Treasury contract implements the escrow mechanism for handling the project budget funds, lock them when work is assigned and release them when work is done
- 

#### Dashboard

- Simple dashboard to perform actions on the work items (issues) for each project
- Token holders can simply approve issues with a signature using their MetaMask (no need for a GitHub account and to understand it)
- Each token holder has a maximum number of votes that can be active at the same time, meaning that when reached voted issues have either to be done or dumped for that vote to be released
- View work by priority, as a result of the approvals each issue has gathered
- 

#### GitHub App

- When a token holder approves an issue on the Dashboard, verify the token holder validity by on-chain balance and signature verification, then update issue with comment detailing it and increment Priority field by token holder balance
- When an admin assigns an issue that has a weight already, or the other way around, send lock transaction to the Treasury smart-contract with payee and the respective amount for the issue weight
- When an admin closes an issue that has a PR or more merged to default branch, then the work is considered accepted and a release transaction is sent to the Treasury smart-contract with payee and amount, so that the value is unlocked and transferred
- 


[TBC]
