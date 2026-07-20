# <img src="https://images.mindcloud.co/apps/icons/etherscan_1776265436336.png" alt="Etherscan logo" width="28" height="28"> Etherscan: Universal API

Etherscan API integration for Ethereum and supported EVM chains.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/etherscan/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://etherscan.io/
- **Vendor API docs:** https://docs.etherscan.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [eth_blockNumber](actions/eth-block-number.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/etherscan/latest/actions/eth-block-number?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [eth_getTransactionCount](actions/eth-get-transaction-count.md) | GET | Retrieves an address transaction count from Etherscan. |
| [Get Address ERC20 Token Holding](actions/get-address-erc20-token-holding.md) | GET | Retrieves ERC20 token holdings for an address. |
| [Get Address ERC721 Token Holding](actions/get-address-erc721-token-holding.md) | GET | Retrieves ERC721 token holdings for an address. |
| [Get Address ERC721 Token Inventory by Contract](actions/get-address-erc721-token-inventory-by-contract.md) | GET | Retrieves ERC721 token inventory by contract for an address. |
| [Get Event Logs by Address](actions/get-event-logs-by-address.md) | GET | Retrieves event logs for an address. |
| [Get Historical Native Balance for an Address](actions/get-historical-native-balance-for-an-address.md) | GET | Retrieves an address's historical native balance from Etherscan. |
| [Get Native Balance for an Address](actions/get-native-balance-for-an-address.md) | GET | Retrieves an address's native balance from Etherscan. |

### Contracts

| Action | Method | Description |
| --- | --- | --- |
| [Get Contract ABI](actions/get-contract-abi.md) | GET | Retrieves a contract ABI from Etherscan. |
| [Get Contract Source Code](actions/get-contract-source-code.md) | GET | Retrieves a contract source code record from Etherscan. |
| [Get ERC20-Token Account Balance for Token Contract Address](actions/get-erc20-token-account-balance-for-token-contract-address.md) | GET | Retrieves an ERC20 token balance for an address. |
| [Get ERC20-Token TotalSupply by Contract Address](actions/get-erc20-token-total-supply-by-contract-address.md) | GET | Retrieves an ERC20 token total supply by contract. |
| [Get Historical ERC20-Token TotalSupply by ContractAddress & BlockNo](actions/get-historical-erc20-token-total-supply-by-contract-address-block-no.md) | GET | Retrieves historical ERC20 token total supply by block. |
| [Get Token Holder Count by Contract Address](actions/get-token-holder-count-by-contract-address.md) | GET | Retrieves the token holder count for a contract. |
| [Get Token Holder List by Contract Address](actions/get-token-holder-list-by-contract-address.md) | GET | Retrieves the token holder list for a contract. |
| [Get Token Info by ContractAddress](actions/get-token-info-by-contract-address.md) | GET | Retrieves token information by contract address. |
| [Get Top Token Holders](actions/get-top-token-holders.md) | GET | Retrieves the top token holders for a contract. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [eth_blockNumber](actions/eth-block-number.md) | GET | Retrieves the latest block number from Etherscan. |
| [eth_gasPrice](actions/eth-gas-price.md) | GET | Retrieves the current gas price from Etherscan. |
| [eth_getBlockByNumber](actions/eth-get-block-by-number.md) | GET | Retrieves a block by number from Etherscan. |
| [eth_getBlockTransactionCountByNumber](actions/eth-get-block-transaction-count-by-number.md) | GET | Retrieves a block transaction count by number. |
| [Get Block and Uncle Rewards by Block Number](actions/get-block-and-uncle-rewards-by-block-number.md) | GET | Retrieves block and uncle rewards by block number. |
| [Get Block Number by Timestamp](actions/get-block-number-by-timestamp.md) | GET | Retrieves a block number by timestamp. |
| [Get Ether Last Price](actions/get-ether-last-price.md) | GET | Retrieves the latest Ether price from Etherscan. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [eth_estimateGas](actions/eth-estimate-gas.md) | GET | Retrieves an estimated gas usage for a transaction. |
| [eth_getTransactionByHash](actions/eth-get-transaction-by-hash.md) | GET | Retrieves a transaction by hash from Etherscan. |
| [Get ERC1155 Token Transfers by Address](actions/get-erc1155-token-transfers-by-address.md) | GET | Retrieves ERC1155 token transfers for an address. |
| [Get ERC20 Token Transfers by Address](actions/get-erc20-token-transfers-by-address.md) | GET | Retrieves ERC20 token transfers for an address. |
| [Get ERC721 Token Transfers by Address](actions/get-erc721-token-transfers-by-address.md) | GET | Retrieves ERC721 token transfers for an address. |
| [Get Internal Transactions by Address](actions/get-internal-transactions-by-address.md) | GET | Retrieves internal transactions for an address. |
| [Get Normal Transactions By Address](actions/get-normal-transactions-by-address.md) | GET | Retrieves normal transactions for an address. |

