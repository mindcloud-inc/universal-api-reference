# List Accounts with SmartReach

Retrieves accounts from SmartReach.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts`
- **Base URL:** `https://api.smartreach.io/api/v3`
- **Official documentation:** [List Accounts](https://help.smartreach.io/reference/accounts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `older_than` | query | `number` | no | timestamp in unix epoch milliseconds |
| `newer_than` | query | `number` | no | timestamp in unix epoch milliseconds |
