# Get Pricing with LimoExpress

Retrieves pricing for coordinates in LimoExpress.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/integration/pricing`
- **Base URL:** `https://api.limoexpress.me`
- **Official documentation:** [Get Pricing](https://api.limoexpress.me/api/docs/v1#/Pricing/getPricing)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_latitude` | query | `number` | yes | FROM latitude coordinate. |
| `from_longitude` | query | `number` | yes | FROM longitude coordinate. |
| `to_latitude` | query | `number` | no | TO latitude coordinate. |
| `to_longitude` | query | `number` | no | TO longitude coordinate. |
| `currency_id` | query | `string` | no | Currency identifier. |
| `vehicle_class_id` | query | `string` | no | Vehicle class identifier. |
| `distance` | query | `number` | no | Distance between start and end locations. |
