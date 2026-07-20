# <img src="https://images.mindcloud.co/apps/icons/1shot-icon_1775757601607.png" alt="1Shot logo" width="28" height="28"> 1Shot: Universal API

1Shot is a full-stack web3 infrastructure platform for onchain agents, workflows, and products, with server wallets, contract methods, delegations, x402, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oneShot/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://1shotapi.com
- **Vendor API docs:** https://docs.1shotapi.com/api/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Chains](actions/list-chains.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-chains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Chain

| Action | Method | Description |
| --- | --- | --- |
| [Get Chain Fees](actions/get-chain-fees.md) | GET | Retrieves chain fee details from 1Shot API. |
| [List Chains](actions/list-chains.md) | GET | Retrieves supported blockchain networks from 1Shot API. |

### Contract

| Action | Method | Description |
| --- | --- | --- |
| [Inspect Contract](actions/inspect-contract.md) | GET | Retrieves contract details from 1Shot API. |

### Contract Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Contract Event](actions/create-contract-event.md) | POST | Creates a new contract event in 1Shot API. |
| [Get Contract Event](actions/get-contract-event.md) | GET | Retrieves contract event details from 1Shot API. |
| [List Contract Events](actions/list-contract-events.md) | GET | Retrieves contract events from 1Shot API. |

### Contract Event Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Contract Event Logs](actions/search-contract-event-logs.md) | GET | Finds contract event logs in 1Shot API. |

### Contract Method

| Action | Method | Description |
| --- | --- | --- |
| [Create Contract Method](actions/create-contract-method.md) | POST | Creates a new contract method endpoint in 1Shot API. |
| [Get Contract Method](actions/get-contract-method.md) | GET | Retrieves contract method endpoint details from 1Shot API. |
| [List Contract Methods](actions/list-contract-methods.md) | GET | Retrieves contract method endpoints from 1Shot API. |

### Contract Method Encode Result

| Action | Method | Description |
| --- | --- | --- |
| [Encode Contract Method](actions/encode-contract-method.md) | GET | Encodes contract method input data in 1Shot API. |

### Contract Method Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Estimate Contract Method](actions/estimate-contract-method.md) | GET | Estimates a contract method transaction in 1Shot API. |

### Contract Method Test Result

| Action | Method | Description |
| --- | --- | --- |
| [Test Contract Method](actions/test-contract-method.md) | GET | Tests a contract method endpoint in 1Shot API. |

### Delegation

| Action | Method | Description |
| --- | --- | --- |
| [Create Delegation](actions/create-delegation.md) | POST | Creates a new wallet delegation in 1Shot API. |
| [List Delegations](actions/list-delegations.md) | GET | Retrieves delegations for a wallet in 1Shot API. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Execute Contract Method](actions/execute-contract-method.md) | POST | Creates a blockchain transaction from a contract method in 1Shot API. |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves transaction details from 1Shot API. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves transaction records from 1Shot API. |
| [Transfer Native Token](actions/transfer-native-token.md) | POST | Creates a native token transfer from a 1Shot API wallet. |

### Wallet

| Action | Method | Description |
| --- | --- | --- |
| [Create Wallet](actions/create-wallet.md) | POST | Creates a new wallet in 1Shot API. |
| [Get Wallet](actions/get-wallet.md) | GET | Retrieves wallet details from 1Shot API. |
| [List Wallets](actions/list-wallets.md) | GET | Retrieves wallet records from 1Shot API. |

### Webhook Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Endpoints](actions/list-webhook-endpoints.md) | GET | Retrieves webhook endpoint configurations from 1Shot API. |

### Webhook Trigger

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Triggers](actions/list-webhook-triggers.md) | GET | Retrieves webhook trigger types from 1Shot API. |

