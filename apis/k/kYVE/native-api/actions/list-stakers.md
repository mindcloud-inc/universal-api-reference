# List Stakers with KYVE

## Endpoint

- **Method:** `GET`
- **Path:** `/kyve/query/v1/stakers`
- **Base URL:** `https://api.kyve.network`
- **Official documentation:** [List Stakers](https://api.kyve.network/static/openapi.yml)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Optional staker status filter. |
| `search` | query | `string` | no | Optional staker moniker or address search. |
