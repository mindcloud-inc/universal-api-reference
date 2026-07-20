# <img src="https://images.mindcloud.co/apps/icons/sps-commerce-corp-2015-logo_1757365700190.png" alt="SPS Commerce logo" width="28" height="28"> SPS Commerce: Universal API

SPS Commerce through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sPSCommerce/latest
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Transaction](actions/get-transaction.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sPSCommerce/latest/actions/get-transaction?connectionId=$CONNECTION_ID&filePath=testout%2FfileName.dat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [List Forms](actions/list-forms.md) | GET |  |
| [List Packing Slip](actions/list-packing-slip.md) | GET |  |
| [List Packing Slips](actions/list-packing-slips.md) | GET |  |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [List Shipping Label by ID](actions/list-shipping-label.md) | GET |  |
| [List Shipping Labels](actions/list-shipping-labels.md) | GET |  |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Create Transaction](actions/create-transaction.md) | POST | This API accepts a payload that initiates a new transaction. |
| [Delete Transaction](actions/delete-transaction.md) | DELETE | Delete a specific transaction file. |
| [Get Transaction](actions/get-transaction.md) | GET | Retrieve a specific file. |
| [List Transaction Histories](actions/list-transaction-histories.md) | GET |  |
| [List Transactions](actions/list-transactions.md) | GET | Get a list of files in a specified directory. |

