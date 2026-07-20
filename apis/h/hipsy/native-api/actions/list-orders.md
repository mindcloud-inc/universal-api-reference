# List Orders with Hipsy

Retrieves orders from a Hipsy organisation.

## Endpoint

- **Method:** `GET`
- **Path:** `/organisation/:organisationSlug/orders`
- **Base URL:** `https://api.hipsy.nl/v1`
- **Official documentation:** [List Orders](https://docs.hipsy.nl/api-reference/list-orders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organisationSlug` | path | `string` | yes | Slug of the organisation whose orders should be listed. |
| `event` | query | `number` | no | Return only orders for a specific event ID. |
