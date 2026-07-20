# Get Payee Location with YNAB

Retrieves a payee location from a YNAB plan.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans/:planId/payee_locations/:payeeLocationId`
- **Base URL:** `https://api.ynab.com/v1`
- **Official documentation:** [Get Payee Location](https://api.ynab.com/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | path | `string` | yes | The id of the plan. You can also use last-used or default when enabled. |
| `payeeLocationId` | path | `string` | yes | The id of the payee location. |
