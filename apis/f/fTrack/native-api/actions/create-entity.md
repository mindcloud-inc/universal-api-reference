# Create Entity with FTrack

Creates an entity in FTrack.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `{serverUrl}`
- **Official documentation:** [Create Entity](https://developer.ftrack.com/api/operations/create-api-create-create-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_type` | body | `string` | yes | Entity type to create. |
| `entity_data` | body | `object` | yes | Entity attributes to create. |
