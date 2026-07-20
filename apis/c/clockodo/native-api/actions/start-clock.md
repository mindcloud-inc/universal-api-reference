# Start Clock with Clockodo

Starts the clock in your Clockodo account.

## Endpoint

- **Method:** `POST`
- **Path:** `/clock`
- **Base URL:** `https://my.clockodo.com/api/v2`
- **Official documentation:** [Start Clock](https://www.clockodo.com/en/api/clock/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `billable` | body | `number` | no | — |
| `customers_id` | body | `string` | yes | Customer ID for the running clock entry. |
| `projects_id` | body | `string` | no | — |
| `text` | body | `string` | no | — |
| `users_id` | body | `string` | no | — |
| `services_id` | body | `string` | yes | Service ID for the running clock entry. |
