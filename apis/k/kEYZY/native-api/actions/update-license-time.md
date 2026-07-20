# Update License Time with KEYZY

Updates start and end times for a KEYZY license.

## Endpoint

- **Method:** `POST`
- **Path:** `/licenses/update-time`
- **Base URL:** `https://api.keyzy.io/v2`
- **Official documentation:** [Update License Time](https://www.keyzy.io/docs/developers/rest-api/licenses-update-time/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_at` | body | `number` | yes | License end time as a Unix timestamp. |
| `serial` | body | `string` | yes | License serial number. |
| `start_at` | body | `number` | no | License start time as a Unix timestamp. |
