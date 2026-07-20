# Create Transaction with Sales Cookie

Creates or updates a transaction in Sales Cookie by unique ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/Api/CreateTransaction`
- **Base URL:** `https://salescookie.com/app`
- **Official documentation:** [Create Transaction](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-use-the-simplified-transaction-import-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | body | `date` | yes | Transaction date in ISO 8601 format. |
| `uniqueId` | body | `string` | yes | Unique transaction identifier. |
| `revenue` | body | `number` | yes | — |
| `currency` | body | `string` | yes | — |
| `transactionStatus` | body | `string` | no | — |
| `owner1` | body | `string` | yes | Primary credited user alias or name. |
| `customer` | body | `string` | no | — |
| `product` | body | `string` | no | — |
