# Get API Usage with KickFire

Retrieves API usage information from KickFire.

## Endpoint

- **Method:** `GET`
- **Path:** `/usage`
- **Base URL:** `https://api.kickfire.com`
- **Official documentation:** [Get API Usage](https://foundryco.com/developers/#api-usage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `edate` | query | `string` | yes | Inclusive usage report end date in YYYY-MM-DD format. |
| `sdate` | query | `string` | yes | Inclusive usage report start date in YYYY-MM-DD format. |
