# Get Order with Humanitix

Retrieves an order for an event from Humanitix.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/orders/:orderId`
- **Base URL:** `https://api.humanitix.com/v1`
- **Official documentation:** [Get Order](https://humanitix.stoplight.io/docs/humanitix-public-api/3be38b97d385c-get-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The Humanitix event ID. |
| `orderId` | path | `string` | yes | The Humanitix order ID. |
