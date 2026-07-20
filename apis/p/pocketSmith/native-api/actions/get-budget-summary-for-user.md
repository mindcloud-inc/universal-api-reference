# Get Budget Summary For User with PocketSmith

Retrieves a budget summary for a PocketSmith user.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:id/budget_summary`
- **Base URL:** `https://api.pocketsmith.com/v2`
- **Official documentation:** [Get Budget Summary For User](https://developers.pocketsmith.com/reference/get_users-id-budget-summary-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_date` | query | `string` | yes | The date to stop analysing the budget from. |
| `id` | path | `number` | yes | The unique identifier of the PocketSmith user. |
| `interval` | query | `number` | yes | The period interval to analyse in. |
| `period` | query | `string` | yes | The period to analyse in. |
| `start_date` | query | `string` | yes | The date to start analysing the budget from. |
