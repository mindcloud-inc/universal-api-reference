# List Credit Transactions with OTO

Retrieves credit transactions from the OTO API.

## Endpoint

- **Method:** `GET`
- **Path:** `/creditTransactions`
- **Base URL:** `https://api.tryoto.com/rest/v2`
- **Official documentation:** [List Credit Transactions](https://help.tryoto.com/en/support/solutions/articles/150000213809-shipments-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `minDate` | query | `date` | yes | Earliest transaction date to include, in YYYY-MM-DD format. |
| `maxDate` | query | `date` | yes | Latest transaction date to include, in YYYY-MM-DD format. |
| `perPage` | query | `number` | no | Maximum number of transactions to return per page. |
| `page` | query | `number` | no | Page number to fetch. |
