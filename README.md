![gitvern logo](https://github.com/gitvern/media/raw/master/logo/logo-text-bg.png)

## DAO Governance based on Github

Features:

- Simple dashboard integrated with Metamask (for any EVM network)
- Issues prioritization by approval of token holders or LPs on Uniswap (each account has a max number of approvals active at any time)
- Dashboard shows prioritized issues at top (based on current holdings of voters)
- Admins assign and attribute weight to the issues and a contract locks the issue funds based on issue weight configuration
- When an admin/maintainer closes an issue with a weight, the respective locked funds are sent to the assignee
- All relevant information is written in issue comments and dashboard parses it and cross references and validates with on-chain data and signatures
- The only data that is kept on-chain are the locked funds and receiver accounts while work is in progress

