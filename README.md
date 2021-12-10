![gitvern logo](https://github.com/gitvern/media/raw/master/logo/logo-text-bg.png)

## DAO Governance based on Github

Enabling easy to implement and use DAO Governance for Open Source development projects, using a governance token in any EVM chain for cost effectiveness.

### System Components:

- [x] [GitHub](#github)
- [x] [DAO Repository](#dao-repository)
- [x] [Smart-Contracts](#smart-contracts)
- [x] [Dashboard](#dashboard)
- [x] [GitHub App](#github-app)

#### GitHub:

- GitHub is the most important piece of this system, as it will serve as contributor interface to most of the activities
- It is suggested to create a GitHub Organization and also the main projects that the DAO will manage, like: Development, Marketing, Social Media, etc
- Then organize the issues (work) under those projects
- We will also install our GitHub App on this Organization, so that we can verify and execute on-chain transactions when some activities take place, and also store off-chain data in GitHub issue comments for future reference and transparency
- 

#### DAO Repository:

[https://github.com/gitvern/dao](https://github.com/gitvern/dao)

- You can find a template DAO Repository [here](https://github.com/gitvern/dao), using gitvern project as an example
- Main DAO public configuration goes here, as it can be accessible from both GitHub App and the Dashboard, e.g., token info, treasury contract, contributor profiles, leader profiles, issue weight payouts, etc
- All this configuration is subject to be agreed in leader meetings, and token holders consulted in an issue if needed
- Also daily administrative activity of the DAO should have it's place here, for instance, meeting minutes, budget approvals, etc
- 

#### Smart-Contracts

[https://github.com/gitvern/contracts](https://github.com/gitvern/contracts)

- Set of smart-contracts to be used as a reference, when deploying each DAO Project's own contracts for:
    - Governance Token contracts
    - Liquidity Building Auction ([LBA](LBA.md)) contracts using a UniSwap Liquidity Pool
    - Treasury Budget distribution contracts using DAO tokens or ETH
- 

#### GitHub App

[https://github.com/gitvern/github-app](https://github.com/gitvern/github-app)

- When a token holder approves an issue on the Dashboard, verify the token holder validity by on-chain balance and signature verification, then update issue with comment detailing it and increment Priority field by token holder balance
- When an admin assigns an issue that has a weight already, or the other way around, send lock transaction to the Treasury smart-contract with payee and the respective amount for the issue weight
- When an admin closes an issue that has a PR or more merged to default branch, then the work is considered accepted and a release transaction is sent to the Treasury smart-contract with payee and amount, so that the value is unlocked and transferred
- 

#### Dashboard

- Integration with [Snapshot.org](https://snapshot.org) dashboard to approve the work items (issues) for each project
- The same dashboard can be used to add and approve other administrative proposals, not related to development issues
- Token holders can simply approve work or proposals with a signature using their MetaMask (no need for a GitHub account or to understand it)
- View work by priority, as a result of the approvals each issue has gathered in GitHub Project board automatically
- 


[TBC]
