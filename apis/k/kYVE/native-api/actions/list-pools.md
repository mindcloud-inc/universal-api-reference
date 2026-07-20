# List Pools with KYVE

## Endpoint

- **Method:** `GET`
- **Path:** `/kyve/query/v1beta1/pools`
- **Base URL:** `https://api.kyve.network`
- **Official documentation:** [List Pools](https://api.kyve.network/static/openapi.yml)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Optional pool search text. |
| `runtime` | query | `string` | no | Optional runtime filter. |
| `disabled` | query | `boolean` | no | Optional disabled-pool filter. |
| `storage_provider_id` | query | `number` | no | Optional storage provider ID filter. |
