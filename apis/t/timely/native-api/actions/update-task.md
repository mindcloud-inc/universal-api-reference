# Update Task with Timely

Updates an existing task in Timely.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/1.1/{account_id}/forecasts/{id}`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [Update Task](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID |
| `id` | path | `number` | yes | Task ID |
| `forecast` | body | `object` | yes | — |
