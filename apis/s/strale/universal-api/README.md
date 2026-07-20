# <img src="https://images.mindcloud.co/apps/icons/strale_1777041800495.png" alt="Strale logo" width="28" height="28"> Strale: Universal API

Run Strale capabilities, search solutions, and verify transactions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/strale/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://strale.dev
- **Vendor API docs:** https://strale.dev/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Wallet Balance](actions/get-wallet-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strale/latest/actions/get-wallet-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Audit Token

| Action | Method | Description |
| --- | --- | --- |
| [Reissue Audit Token](actions/reissue-audit-token.md) | POST | Reissues an audit token for a transaction in Strale. |

### Capability

| Action | Method | Description |
| --- | --- | --- |
| [Get Capability](actions/get-capability.md) | GET | Retrieves a capability from Strale. |
| [List Capabilities](actions/list-capabilities.md) | GET | Retrieves capabilities from Strale. |

### Execution

| Action | Method | Description |
| --- | --- | --- |
| [Execute Capability](actions/execute-capability.md) | POST | Executes a capability in Strale. |
| [Execute Task](actions/execute-task.md) | POST | Executes a task in Strale using semantic matching. |

### Quality Score

| Action | Method | Description |
| --- | --- | --- |
| [Get Capability Quality](actions/get-capability-quality.md) | GET | Retrieves a capability quality score from Strale. |

### Solution

| Action | Method | Description |
| --- | --- | --- |
| [Get Solution](actions/get-solution.md) | GET | Retrieves a solution from Strale. |
| [List Solutions](actions/list-solutions.md) | GET | Retrieves solutions from Strale. |

### Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Suggest Capability](actions/suggest-capability.md) | GET | Suggests capabilities or solutions in Strale for a query. |
| [Typeahead Search](actions/typeahead-search.md) | GET | Finds capabilities or solutions in Strale by keyword. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieves a transaction from Strale. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves transactions from Strale. |

### Transaction Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Transaction Integrity](actions/verify-transaction-integrity.md) | GET | Verifies a transaction integrity trail in Strale. |

### Wallet Balance

| Action | Method | Description |
| --- | --- | --- |
| [Get Wallet Balance](actions/get-wallet-balance.md) | GET | Retrieves your wallet balance from Strale. |

### Wallet Top-up

| Action | Method | Description |
| --- | --- | --- |
| [Create Wallet Top-Up](actions/create-wallet-top-up.md) | POST | Creates a wallet top-up checkout session in Strale. |

### Wallet Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Wallet Transactions](actions/list-wallet-transactions.md) | GET | Retrieves wallet transactions from Strale. |

