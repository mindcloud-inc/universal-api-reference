# List Email Settings with SmartReach

Retrieves email settings from SmartReach.

## Endpoint

- **Method:** `GET`
- **Path:** `/email_settings`
- **Base URL:** `https://api.smartreach.io/api/v3`
- **Official documentation:** [List Email Settings](https://help.smartreach.io/reference/get_email-settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `older_than` | query | `number` | no | timestamp in unix epoch milliseconds |
| `newer_than` | query | `number` | no | timestamp in unix epoch milliseconds |
