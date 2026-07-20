# Update Time Entry with Timely

Updates an existing time entry in Timely.

## Endpoint

- **Method:** `PUT`
- **Path:** `/1.1/{account_id}/hours/{id}`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [Update Time Entry](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID |
| `id` | path | `number` | yes | Time entry ID |
| `event` | body | `object` | yes | — |
