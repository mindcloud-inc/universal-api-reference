# List Available Slots with Vyte

Retrieves available slots from Vyte.

## Endpoint

- **Method:** `GET`
- **Path:** `v2/slots`
- **Base URL:** `https://api.vyte.in`
- **Official documentation:** [List Available Slots](https://developer.vyte.in/reference/slots/#list-slots)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `duration` | query | `string` | no | Meeting duration in minutes. |
| `emails` | query | `string` | no | Comma-separated email list to evaluate availability for. |
| `from` | query | `string` | no | Start date or datetime for the search window. |
| `to` | query | `string` | no | End date or datetime for the search window. |
