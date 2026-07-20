# List Finalized Bundles with KYVE

## Endpoint

- **Method:** `GET`
- **Path:** `/kyve/v1/bundles/{pool_id}`
- **Base URL:** `https://api.kyve.network`
- **Official documentation:** [List Finalized Bundles](https://api.kyve.network/static/openapi.yml)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pool_id` | path | `string` | yes | Pool ID to list finalized bundles for. |
| `index` | query | `string` | no | Optional bundle index filter; cannot be combined with pagination. |
