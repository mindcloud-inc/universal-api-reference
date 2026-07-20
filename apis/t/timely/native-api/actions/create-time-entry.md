# Create Time Entry with Timely

Creates a time entry in Timely.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.1/{account_id}/hours`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [Create Time Entry](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID where the time entry will be created |
| `event` | body | `object` | yes | — |
