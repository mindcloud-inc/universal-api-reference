# Get Tracking Link with Shippify

Retrieves a secure delivery tracking link from Shippify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/deliveries/token/:id`
- **Base URL:** `https://api.shippify.co`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Shippify delivery identifier or reference ID to retrieve the tracking link for. |
