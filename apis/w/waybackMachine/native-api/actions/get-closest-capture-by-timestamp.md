# Get Closest Capture By Timestamp with Wayback Machine

Retrieves the closest archived capture to a timestamp in Wayback Machine.

## Endpoint

- **Method:** `GET`
- **Path:** `/wayback/available`
- **Base URL:** `https://archive.org`
- **Official documentation:** [Get Closest Capture By Timestamp](https://archive.org/help/wayback_api.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The live URL to search for in the Wayback Machine archive. |
| `timestamp` | query | `string` | yes | Wayback timestamp to search near, using 1 to 14 digits in YYYYMMDDhhmmss order. |
