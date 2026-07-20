# List Payee Locations with YNAB

Retrieves payee locations from a YNAB plan.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans/:planId/payee_locations`
- **Base URL:** `https://api.ynab.com/v1`
- **Official documentation:** [List Payee Locations](https://api.ynab.com/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | path | `string` | yes | The id of the plan. You can also use last-used or default when enabled. |
