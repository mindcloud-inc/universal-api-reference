# Update Pickup Point with Shippify

Updates pickup details for deliveries in Shippify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/deliveries/pickup`
- **Base URL:** `https://api.shippify.co`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deliveryIds` | body | `string` | yes | Comma-separated Shippify delivery identifiers to update, up to 10 per request. |
| `deliveryChanges` | body | `object` | yes | Required object describing pickup contact and or pickup location changes. |
| `recalculatePrice` | body | `boolean` | yes | Whether Shippify should recalculate the delivery price after the update. |
| `reorderRoute` | body | `boolean` | yes | Whether Shippify should reorder the route after the update when the delivery belongs to a route. |
