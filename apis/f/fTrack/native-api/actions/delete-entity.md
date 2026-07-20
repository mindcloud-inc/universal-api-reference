# Delete Entity with FTrack

Deletes an entity from FTrack.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `{serverUrl}`
- **Official documentation:** [Delete Entity](https://developer.ftrack.com/api/operations/delete-api-delete-delete-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_type` | body | `string` | yes | Entity type to delete. |
| `entity_key` | body | `string` | yes | Key or id identifying the entity to delete. |
