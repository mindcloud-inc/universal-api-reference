# <img src="https://images.mindcloud.co/apps/icons/unnamed_1773952590422.png" alt="Airwallex logo" width="28" height="28"> Airwallex: Universal API

Manage balances, beneficiaries, transfers, and payment links

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/airwallex/latest
- **Category:** Commerce / Accounting
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.airwallex.com
- **Vendor API docs:** https://www.airwallex.com/docs/developer-tools/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Balances](actions/get-current-balances.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/get-current-balances?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Obtain Access Token](actions/obtain-access-token.md) | POST | Creates an API access token in Airwallex. |

### Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Balances](actions/get-current-balances.md) | GET | Retrieves current balances for a connected Airwallex account. |

### Bank Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Get Beneficiary by ID](actions/get-beneficiary-by-id.md) | GET | Retrieves a beneficiary by ID from Airwallex. |
| [Get Global Account by ID](actions/get-global-account-by-id.md) | GET | Retrieves a global account by ID from Airwallex. |
| [List Beneficiaries](actions/list-beneficiaries.md) | GET | Retrieves saved payout beneficiaries from Airwallex. |
| [List Global Accounts](actions/list-global-accounts.md) | GET | Retrieves global account records from Airwallex. |
| [List Supported Beneficiary Banks](actions/list-supported-beneficiary-banks.md) | GET | Retrieves supported beneficiary banks from Airwallex. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Create Transfer](actions/create-transfer.md) | POST | Creates a new payout transfer in Airwallex. |
| [Get Transfer by ID](actions/get-transfer-by-id.md) | GET | Retrieves a transfer by ID from Airwallex. |
| [List Transfers](actions/list-transfers.md) | GET | Retrieves payout transfer records from Airwallex. |
| [Validate Transfer](actions/validate-transfer.md) | GET | Validates transfer details in Airwallex before payout creation. |

