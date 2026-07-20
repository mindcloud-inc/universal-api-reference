# Check URL Availability with Wayback Machine

Retrieves archived snapshot availability for a URL in Wayback Machine.

## Endpoint

- **Method:** `GET`
- **Path:** `/wayback/available`
- **Base URL:** `https://archive.org`
- **Official documentation:** [Check URL Availability](https://archive.org/help/wayback_api.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The live URL to check in the Wayback Machine archive. |
| `timestamp` | query | `string` | no | Optional Wayback timestamp to search near, using 1 to 14 digits in YYYYMMDDhhmmss order. |
