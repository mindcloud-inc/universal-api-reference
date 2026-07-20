# Get Order with Eventbrite

Retrieves an order from Eventbrite.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/:orderId/`
- **Base URL:** `https://www.eventbriteapi.com/v3`
- **Official documentation:** [Get Order](https://www.eventbrite.com/platform/docs/order-lookup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | Eventbrite order identifier (for example, 14395036633). |
