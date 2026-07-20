# Get Account with YNAB

Retrieves an account from a YNAB plan.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans/:planId/accounts/:accountId`
- **Base URL:** `https://api.ynab.com/v1`
- **Official documentation:** [Get Account](https://api.ynab.com/v1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `planId` | path | `string` | yes |
| `accountId` | path | `string` | yes |
