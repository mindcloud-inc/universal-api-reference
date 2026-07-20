# List Entities with Mem0

Retrieves entities from Mem0.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/entities/`
- **Base URL:** `https://api.mem0.ai`
- **Official documentation:** [List Entities](https://docs.mem0.ai/api-reference/entities/get-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_type` | query | `string` | no | Mem0 entity type filter when supported. |
| `org_id` | query | `string` | no | Mem0 organization ID filter when supported. |
| `project_id` | query | `string` | no | Mem0 project ID filter when supported. |
