# Remove Deliveries From Route with Shippify

Removes deliveries from an existing route in Shippify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/routes/remove`
- **Base URL:** `https://api.shippify.co`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `routeId` | body | `string` | yes | Identifier of the route that the deliveries should be removed from. |
| `deliveries[]` | body | `array<string>` | yes | Required array of delivery identifiers to remove from the route. |
