# Break Route with Shippify

Deletes routes in Shippify and returns deliveries to processing.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/routes/destroy`
- **Base URL:** `https://api.shippify.co`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `routes[]` | body | `array<string>` | yes | Required array of route identifiers to break. |
