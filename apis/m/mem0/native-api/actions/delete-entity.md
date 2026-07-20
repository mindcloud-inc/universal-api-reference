# Delete Entity with Mem0

Deletes an entity from Mem0.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/entities/:entity_type/:entity_id/`
- **Base URL:** `https://api.mem0.ai`
- **Official documentation:** [Delete Entity](https://docs.mem0.ai/api-reference/entities/delete-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_type` | path | `string` | yes | Mem0 entity type from the entity resource path. |
| `entity_id` | path | `string` | yes | Mem0 entity ID from the entity resource path. |
