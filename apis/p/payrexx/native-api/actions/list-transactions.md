# List Transactions with Payrexx

Retrieves transactions from Payrexx.

## Endpoint

- **Method:** `GET`
- **Path:** `Transaction/`
- **Base URL:** `https://api.payrexx.com/v1.14/`
- **Official documentation:** [List Transactions](https://developers.payrexx.com/reference/retrieve-transactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filterDatetimeUtcGreaterThan` | body | `date` | no | Lower DateTime limit in the format YYYY-MM-DD HH:MM:SS. |
| `filterDatetimeUtcLessThan` | body | `date` | no | Upper DateTime limit in the format YYYY-MM-DD HH:MM:SS. |
| `filterMyTransactionsOnly` | body | `boolean` | no | When true, only transactions related to this API key are returned. |
| `orderByTime` | body | `string` | no | ASC or DESC for ordering by time of the transaction. |
| `offset` | body | `number` | no | Row count to be used as offset. |
| `limit` | body | `number` | no | Max row count. |
