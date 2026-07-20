# List Team Available Slots with Vyte

Retrieves available team slots from Vyte.

## Endpoint

- **Method:** `GET`
- **Path:** `v2/slots`
- **Base URL:** `https://api.vyte.in`
- **Official documentation:** [List Team Available Slots](https://developer.vyte.in/guides/setup-team-booking/#get-available-slots-for-your-team)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `duration` | query | `string` | no | Meeting duration in minutes. |
| `from` | query | `string` | no | Start date or datetime for the search window. |
| `team` | query | `string` | no | Return slots for this team. |
| `to` | query | `string` | no | End date or datetime for the search window. |
