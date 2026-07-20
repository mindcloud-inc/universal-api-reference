# List transactions with Atlar

Retrieves transactions from Atlar.

## Endpoint

- **Method:** `GET`
- **Path:** `/financial-data/v2/transactions`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [List transactions](https://docs.atlar.com/reference/get-financial-data-v2-transactions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | query | `string<string>` | no |
| `reconciliationStatus` | query | `string<string>` | no |
| `date` | query | `string<string>` | no |
