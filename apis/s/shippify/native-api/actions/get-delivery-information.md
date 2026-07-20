# Get Delivery Information with Shippify

Retrieves delivery details from Shippify by ID or reference.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/deliveries/:id/complete`
- **Base URL:** `https://api.shippify.co`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Shippify delivery identifier or reference ID to query. |
