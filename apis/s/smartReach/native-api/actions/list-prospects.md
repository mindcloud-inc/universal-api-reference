# List Prospects with SmartReach

Retrieves prospects from SmartReach.

## Endpoint

- **Method:** `GET`
- **Path:** `/prospects`
- **Base URL:** `https://api.smartreach.io/api/v3`
- **Official documentation:** [List Prospects](https://help.smartreach.io/reference/getprospects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `older_than` | query | `number` | no | timestamp in unix epoch milliseconds |
| `newer_than` | query | `number` | no | timestamp in unix epoch milliseconds |
