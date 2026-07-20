# Etherscan: Native API Reference

A consolidated summary of Etherscan's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.etherscan.io/
- **API base URL:** `https://api.etherscan.io`

## Authentication

### API Key

Provider-native API key required. Activation can take several minutes after creation, and some dashboard flows may still require manual provider access.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.etherscan.io/)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [eth_blockNumber](actions/eth-block-number.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/ethblocknumber) |
| [eth_estimateGas](actions/eth-estimate-gas.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/ethestimategas) |
| [eth_gasPrice](actions/eth-gas-price.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/ethgasprice) |
| [eth_getBlockByNumber](actions/eth-get-block-by-number.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/ethgetblockbynumber) |
| [eth_getBlockTransactionCountByNumber](actions/eth-get-block-transaction-count-by-number.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/ethgetblocktransactioncountbynumber) |
| [eth_getTransactionByHash](actions/eth-get-transaction-by-hash.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/ethgettransactionbyhash) |
| [eth_getTransactionCount](actions/eth-get-transaction-count.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/ethgettransactioncount) |
| [Get Address ERC20 Token Holding](actions/get-address-erc20-token-holding.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/addresstokenbalance) |
| [Get Address ERC721 Token Holding](actions/get-address-erc721-token-holding.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/addresstokennftbalance) |
| [Get Address ERC721 Token Inventory by Contract](actions/get-address-erc721-token-inventory-by-contract.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/addresstokennftinventory) |
| [Get Block and Uncle Rewards by Block Number](actions/get-block-and-uncle-rewards-by-block-number.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/getblockreward) |
| [Get Block Number by Timestamp](actions/get-block-number-by-timestamp.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/getblocknobytime) |
| [Get Contract ABI](actions/get-contract-abi.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/getabi) |
| [Get Contract Source Code](actions/get-contract-source-code.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/getsourcecode) |
| [Get ERC1155 Token Transfers by Address](actions/get-erc1155-token-transfers-by-address.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/token1155tx) |
| [Get ERC20-Token Account Balance for Token Contract Address](actions/get-erc20-token-account-balance-for-token-contract-address.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/tokenbalance) |
| [Get ERC20-Token TotalSupply by Contract Address](actions/get-erc20-token-total-supply-by-contract-address.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/etherscan-v2/api-endpoints/tokens) |
| [Get ERC20 Token Transfers by Address](actions/get-erc20-token-transfers-by-address.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/tokentx) |
| [Get ERC721 Token Transfers by Address](actions/get-erc721-token-transfers-by-address.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/tokennfttx) |
| [Get Ether Last Price](actions/get-ether-last-price.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/ethprice) |
| [Get Event Logs by Address](actions/get-event-logs-by-address.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/getlogs) |
| [Get Historical ERC20-Token TotalSupply by ContractAddress & BlockNo](actions/get-historical-erc20-token-total-supply-by-contract-address-block-no.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/tokensupplyhistory) |
| [Get Historical Native Balance for an Address](actions/get-historical-native-balance-for-an-address.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/balancehistory) |
| [Get Internal Transactions by Address](actions/get-internal-transactions-by-address.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/txlistinternal) |
| [Get Native Balance for an Address](actions/get-native-balance-for-an-address.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/balance) |
| [Get Normal Transactions By Address](actions/get-normal-transactions-by-address.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/txlist) |
| [Get Token Holder Count by Contract Address](actions/get-token-holder-count-by-contract-address.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/tokenholdercount) |
| [Get Token Holder List by Contract Address](actions/get-token-holder-list-by-contract-address.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/tokenholderlist) |
| [Get Token Info by ContractAddress](actions/get-token-info-by-contract-address.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/tokeninfo) |
| [Get Top Token Holders](actions/get-top-token-holders.md) | `GET /v2/api` | [docs](https://docs.etherscan.io/api-reference/endpoint/toptokenholders) |
