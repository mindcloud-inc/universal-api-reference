# <img src="https://images.mindcloud.co/apps/icons/favicon-docs-overledger-dev-48x48_1777919311459.png" alt="Overledger logo" width="28" height="28"> Overledger: Universal API

Build blockchain workflows with Quant Overledger APIs for supported tokens, smart contracts, transactions, account searches, and webhooks across supported networks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/overledger/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://quant.network/overledger-platform/
- **Vendor API docs:** https://docs.overledger.dev/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Supported Fungible Tokens](actions/list-supported-fungible-tokens.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/overledger/latest/actions/list-supported-fungible-tokens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Account Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Update Account Webhook Callback URL](actions/update-account-webhook-callback-url.md) | PUT |  |

### Address Sequence

| Action | Method | Description |
| --- | --- | --- |
| [Get Address Sequence](actions/get-address-sequence.md) | GET |  |

### Fungible Token

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Fungible Tokens](actions/list-supported-fungible-tokens.md) | GET |  |

### Smart Contract Read

| Action | Method | Description |
| --- | --- | --- |
| [Read Smart Contract Function](actions/read-smart-contract-function.md) | GET |  |

### Smart Contract Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Smart Contract Webhook](actions/create-smart-contract-webhook.md) | POST |  |

### Utxo State

| Action | Method | Description |
| --- | --- | --- |
| [Get UTXO State](actions/get-utxo-state.md) | GET |  |

