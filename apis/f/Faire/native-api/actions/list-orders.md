# List Orders with Faire

## Endpoint

- **Method:** `GET`
- **Path:** `orders`
- **Base URL:** `https://www.faire.com/external-api/v2/`
- **Official documentation:** [List Orders](https://faire.github.io/external-api-docs/#get-all-orders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sortBy` | query | `list<string>` | no | Accepted values: `CREATED_AT`, `UPDATED_AT`. |
| `created_at_min` | query | `string` | no | — |
| `excluded_states` | query | `string` | no | — |
| `ship_after_max` | query | `string` | no | — |
| `updated_at_min` | query | `string` | no | — |
