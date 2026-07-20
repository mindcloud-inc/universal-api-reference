# List Participants By Order with Sympla

Retrieves participants from Sympla for a specific order.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/orders/:orderId/participants`
- **Base URL:** `https://api.sympla.com.br/public/v1.5.1`
- **Official documentation:** [List Participants By Order](https://developers.sympla.com.br/api-doc/index.html#operation/getAllParticipantsForOrder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | Unique identifier of the event. |
| `orderId` | path | `string` | yes | Unique identifier of the order within the event. |
| `fields` | query | `string` | no | Optional comma-separated response fields to include. |
