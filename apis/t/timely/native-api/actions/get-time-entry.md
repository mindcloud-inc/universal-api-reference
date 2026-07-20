# Get Time Entry with Timely

Retrieves a time entry from Timely.

## Endpoint

- **Method:** `GET`
- **Path:** `/1.1/{account_id}/hours/{id}`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [Get Time Entry](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID |
| `id` | path | `number` | yes | Time entry ID |
