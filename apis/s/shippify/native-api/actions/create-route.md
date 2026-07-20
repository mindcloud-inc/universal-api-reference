# Create Route with Shippify

Creates delivery routes in Shippify asynchronously.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/routes/create`
- **Base URL:** `https://api.shippify.co`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `routes[]` | body | `array<object>` | yes | Required array of route definitions. Each item follows Shippify's documented route object containing deliveries and route metadata. |
| `iterations` | body | `number` | yes | Required number of optimization iterations Shippify should run when creating the route. |
