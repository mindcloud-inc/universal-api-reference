# Update Delivery with Shippify

Updates delivery details in Shippify by ID or reference.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/deliveries/dropoff`
- **Base URL:** `https://api.shippify.co`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deliveryIds[]` | body | `array<string>` | yes | Required array of up to 10 Shippify delivery identifiers to update. |
| `referenceIds[]` | body | `array<string>` | no | Optional array of delivery reference identifiers to update instead of delivery IDs. |
| `deliveryChanges` | body | `object` | yes | Required object describing the delivery fields to update, such as dropoff, packages, tags, cod, or referenceId. |
| `recalculatePrice` | body | `boolean` | no | Whether Shippify should recalculate the delivery price after the update. |
| `reorderRoute` | body | `boolean` | no | Whether Shippify should reorder the route after the update when the delivery belongs to a route. |
| `recalculateCity` | body | `boolean` | no | Whether Shippify should recalculate the city after the update. |
