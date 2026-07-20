# Move Item To Another List with DataMerge

Moves an item to another DataMerge list.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/lists/:object_type/:list/:item_id/move`
- **Base URL:** `https://api.datamerge.ai`
- **Official documentation:** [Move Item To Another List](https://api.datamerge.ai/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `object_type` | path | `string` | yes |
| `list` | path | `string` | yes |
| `item_id` | path | `string` | yes |
| `target_list` | body | `string` | yes |
