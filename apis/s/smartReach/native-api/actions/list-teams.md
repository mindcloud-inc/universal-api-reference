# List Teams with SmartReach

Retrieves teams from SmartReach.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams`
- **Base URL:** `https://api.smartreach.io/api/v3`
- **Official documentation:** [List Teams](https://help.smartreach.io/reference/getteams)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | query | `boolean` | no | Filter teams by active = true/false. Default is active=true |
| `older_than` | query | `number` | no | timestamp in unix epoch milliseconds |
| `newer_than` | query | `number` | no | timestamp in unix epoch milliseconds |
