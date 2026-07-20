# List invocations with Chroma Cloud

Retrieves invocations from Chroma Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `https://sync.trychroma.com/api/v1/invocations`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [List invocations](https://docs.trychroma.com/reference/sync-api/invocation/list-invocations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `source_id` | query | `string` | no |
| `status` | query | `string` | no |
| `order_by` | query | `string` | no |
