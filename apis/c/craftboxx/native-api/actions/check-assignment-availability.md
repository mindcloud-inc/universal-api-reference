# Check Assignment Availability with Craftboxx

Returns unavailable assignment master data for a date range from Craftboxx.

## Endpoint

- **Method:** `GET`
- **Path:** `assignments/check-availability`
- **Base URL:** `https://api.craftboxx.de`
- **Official documentation:** [Check Assignment Availability](https://api.craftboxx.de/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | query | `string` | no | The interval end timestamp. |
| `exclude` | query | `string` | no | Optional assignment ID to exclude from the availability check. |
| `start` | query | `string` | no | The interval start timestamp. |
