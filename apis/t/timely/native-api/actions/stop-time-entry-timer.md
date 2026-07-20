# Stop Time Entry Timer with Timely

Stops the timer for an existing time entry in Timely.

## Endpoint

- **Method:** `PUT`
- **Path:** `/1.1/{account_id}/hours/{id}/stop`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [Stop Time Entry Timer](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID |
| `id` | path | `number` | yes | Time entry ID |
