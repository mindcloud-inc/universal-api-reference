# List Transactions with TemplateFox

Retrieves account transactions from TemplateFox.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/account/transactions`
- **Base URL:** `https://api.templatefox.com`
- **Official documentation:** [List Transactions](https://templatefox.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Number of transactions to return. |
| `offset` | query | `number` | no | Number of transactions to skip. |
