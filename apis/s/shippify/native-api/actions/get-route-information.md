# Get Route Information with Shippify

Retrieves route details from Shippify by route or delivery ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/routes/:id`
- **Base URL:** `https://api.shippify.co`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Route identifier to query, or a delivery ID that belongs to the route. |
