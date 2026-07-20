# Get Storage Usage with FTrack

Retrieves storage usage from FTrack.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `{serverUrl}`
- **Official documentation:** [Get Storage Usage](https://developer.ftrack.com/api/operations/storage-usage-api-storage-usage-storageusage-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_type` | body | `string` | no | Optional entity type to scope storage usage. |
| `entity_id` | body | `string` | no | Optional entity id to scope storage usage. |
