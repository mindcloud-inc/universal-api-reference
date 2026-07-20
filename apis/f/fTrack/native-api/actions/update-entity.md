# Update Entity with FTrack

Updates an entity in FTrack.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `{serverUrl}`
- **Official documentation:** [Update Entity](https://developer.ftrack.com/api/operations/update-api-update-update-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_type` | body | `string` | yes | Entity type to update. |
| `entity_key` | body | `string` | yes | Key or id identifying the entity to update. |
| `entity_data` | body | `object` | yes | Attributes to update on the entity. |
