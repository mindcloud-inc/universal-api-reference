# List Slot Days with Vyte

Retrieves slot days from Vyte.

## Endpoint

- **Method:** `GET`
- **Path:** `v2/slots/days`
- **Base URL:** `https://api.vyte.in`
- **Official documentation:** [List Slot Days](https://developer.vyte.in/reference/slots/#list-slots-days)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `duration` | query | `string` | no | Meeting duration in minutes. |
| `emails` | query | `string` | no | Comma-separated email list to evaluate daily availability for. |
| `from` | query | `string` | no | Start date or datetime for the search window. |
| `to` | query | `string` | no | End date or datetime for the search window. |
