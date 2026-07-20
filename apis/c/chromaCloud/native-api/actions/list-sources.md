# List sources with Chroma Cloud

Retrieves sources from Chroma Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `https://sync.trychroma.com/api/v1/sources`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [List sources](https://docs.trychroma.com/reference/sync-api/source/list-sources)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `source_type` | query | `string` | no |
| `order_by` | query | `string` | no |
