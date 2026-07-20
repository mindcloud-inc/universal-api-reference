# Get Payee with YNAB

Retrieves a payee from a YNAB plan.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans/:planId/payees/:payeeId`
- **Base URL:** `https://api.ynab.com/v1`
- **Official documentation:** [Get Payee](https://api.ynab.com/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | path | `string` | yes | The id of the plan. You can also use last-used or default when enabled. |
| `payeeId` | path | `string` | yes | The id of the payee. |
