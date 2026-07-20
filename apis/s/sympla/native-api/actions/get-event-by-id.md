# Get Event By ID with Sympla

Retrieves an event from Sympla by event ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId`
- **Base URL:** `https://api.sympla.com.br/public/v1.5.1`
- **Official documentation:** [Get Event By ID](https://developers.sympla.com.br/api-doc/index.html#operation/getEventId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | Unique identifier of the event. |
| `fields` | query | `string` | no | Optional comma-separated response fields to include. |
