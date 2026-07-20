# Get Transaction with YNAB

Retrieves a transaction from a YNAB plan.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans/:planId/transactions/:transactionId`
- **Base URL:** `https://api.ynab.com/v1`
- **Official documentation:** [Get Transaction](https://api.ynab.com/v1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `planId` | path | `string` | yes |
| `transactionId` | path | `string` | yes |
