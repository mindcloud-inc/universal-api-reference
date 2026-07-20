# List Orders By Event with Sympla

Retrieves orders from Sympla for a specific event.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/orders`
- **Base URL:** `https://api.sympla.com.br/public/v1.5.1`
- **Official documentation:** [List Orders By Event](https://developers.sympla.com.br/api-doc/index.html#operation/getListOrders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | Unique identifier of the event. |
| `fields` | query | `string` | no | Optional comma-separated response fields to include. |
