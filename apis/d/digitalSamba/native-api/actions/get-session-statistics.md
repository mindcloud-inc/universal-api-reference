# Get session statistics with Digital Samba

Retrieves session statistics from Digital Samba.

## Endpoint

- **Method:** `GET`
- **Path:** `/sessions/:session`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Get session statistics](https://developer.digitalsamba.com/rest-api/#statistics-GETapi-v1-sessions--session--statistics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session` | path | `string` | yes | Session path parameter. |
| `metrics` | query | `string` | no | Metrics in the result dataset, set field names under comma (Ex: participation_minutes,broadcasted_minutes,subscribed_minutes). |
