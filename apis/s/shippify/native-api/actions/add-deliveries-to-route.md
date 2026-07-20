# Add Deliveries To Route with Shippify

Adds deliveries to an existing route in Shippify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/routes/add`
- **Base URL:** `https://api.shippify.co`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `routeId` | body | `string` | yes | Identifier of the route that should receive the deliveries. |
| `deliveries[]` | body | `array<string>` | yes | Required array of delivery identifiers to add to the route. |
