# Get Plan Settings with YNAB

Retrieves plan settings from YNAB.

## Endpoint

- **Method:** `GET`
- **Path:** `/plans/:planId/settings`
- **Base URL:** `https://api.ynab.com/v1`
- **Official documentation:** [Get Plan Settings](https://api.ynab.com/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | path | `string` | yes | The id of the plan. You can also use last-used or default when enabled. |
