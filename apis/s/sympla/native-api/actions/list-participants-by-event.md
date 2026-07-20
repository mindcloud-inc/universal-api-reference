# List Participants By Event with Sympla

Retrieves participants from Sympla for a specific event.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/participants`
- **Base URL:** `https://api.sympla.com.br/public/v1.5.1`
- **Official documentation:** [List Participants By Event](https://developers.sympla.com.br/api-doc/index.html#operation/getAllParticipants)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | Unique identifier of the event. |
| `fields` | query | `string` | no | Optional comma-separated response fields to include. |
