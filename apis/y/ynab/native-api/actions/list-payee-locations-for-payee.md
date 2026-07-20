# List Payee Locations For Payee with YNAB

Retrieves payee locations for a payee in YNAB.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans/:planId/payees/:payeeId/payee_locations`
- **Base URL:** `https://api.ynab.com/v1`
- **Official documentation:** [List Payee Locations For Payee](https://api.ynab.com/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | path | `string` | yes | The id of the plan. You can also use last-used or default when enabled. |
| `payeeId` | path | `string` | yes | The id of the payee. |
