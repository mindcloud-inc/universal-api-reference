# List Road Events with National Park Service

Retrieves road events from National Park Service.

## Endpoint

- **Method:** `GET`
- **Path:** `/roadevents`
- **Base URL:** `https://developer.nps.gov/api/v1`
- **Official documentation:** [List Road Events](https://www.nps.gov/subjects/developer/api-documentation.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parkCode` | query | `string` | no | NPS park code. |
| `type` | query | `string` | no | Road event type, such as incident or workzone. |
