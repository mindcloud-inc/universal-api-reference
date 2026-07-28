# <img src="https://images.mindcloud.co/apps/icons/ramp-icon_1782394333561.jpg" alt="Ramp logo" width="28" height="28"> Ramp: Universal API

Ramp through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ramp/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor API docs:** https://docs.ramp.com/developer-api/v1/overview/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Vendors](actions/list-vendors.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ramp/latest/actions/list-vendors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET |  |
| [List Vendors](actions/list-vendors.md) | GET |  |

### Receipts

| Action | Method | Description |
| --- | --- | --- |
| [List Receipts](actions/list-receipts.md) | GET |  |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Get Transaction](actions/get-transaction.md) | GET |  |
| [List Transactions](actions/list-transactions.md) | GET |  |
| [Upload a new memo for a transaction](actions/upload-transaction-memo.md) | PUT |  |

