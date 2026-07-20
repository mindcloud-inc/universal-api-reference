# Get Order By ID with Sympla

Retrieves an order from Sympla by order ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/orders/:orderId`
- **Base URL:** `https://api.sympla.com.br/public/v1.5.1`
- **Official documentation:** [Get Order By ID](https://developers.sympla.com.br/api-doc/index.html#operation/getOneOrder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | Unique identifier of the event. |
| `orderId` | path | `string` | yes | Unique identifier of the order within the event. |
| `fields` | query | `string` | no | Optional comma-separated response fields to include. |
