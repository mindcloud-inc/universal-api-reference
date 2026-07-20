# List Users with SmartReach

Retrieves users from SmartReach.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://api.smartreach.io/api/v3`
- **Official documentation:** [List Users](https://help.smartreach.io/reference/getusers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `older_than` | query | `number` | no | timestamp in unix epoch milliseconds |
| `newer_than` | query | `number` | no | timestamp in unix epoch milliseconds |
