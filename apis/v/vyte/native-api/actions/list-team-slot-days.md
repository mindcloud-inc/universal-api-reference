# List Team Slot Days with Vyte

Retrieves team slot days from Vyte.

## Endpoint

- **Method:** `GET`
- **Path:** `v2/slots/days`
- **Base URL:** `https://api.vyte.in`
- **Official documentation:** [List Team Slot Days](https://developer.vyte.in/reference/slots/#list-slots-days)

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
| `team` | query | `string` | no | Return available days for this team. |
| `to` | query | `string` | no | End date or datetime for the search window. |
