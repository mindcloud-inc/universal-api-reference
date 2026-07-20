# Get List Members with DataMerge

Retrieves items from a specific DataMerge list.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/lists/:object_type/:list`
- **Base URL:** `https://api.datamerge.ai`
- **Official documentation:** [Get List Members](https://api.datamerge.ai/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `object_type` | path | `string` | yes | List object type. |
| `list` | path | `string` | yes | List slug. |
| `page` | query | `number` | no | Page number. |
| `page_size` | query | `number` | no | Page size. |
| `sort_by` | query | `string` | no | Sort field. |
| `sort_order` | query | `string` | no | Sort order. |
