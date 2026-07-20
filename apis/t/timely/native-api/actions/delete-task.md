# Delete Task with Timely

Deletes an existing task from Timely.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/1.1/{account_id}/forecasts/{id}`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [Delete Task](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID |
| `id` | path | `number` | yes | Task ID |
