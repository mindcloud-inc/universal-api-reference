# Convert Entity Type with FTrack

Converts an entity type in FTrack.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `{serverUrl}`
- **Official documentation:** [Convert Entity Type](https://developer.ftrack.com/api/operations/convert-entity-api-convert-entity-convertentity-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_type` | body | `string` | yes | Current entity type. |
| `entity_key` | body | `string` | yes | Key or id identifying the entity to convert. |
| `target_entity_type` | body | `string` | yes | Entity type to convert the record into. |
| `entity_data` | body | `object` | no | Optional attributes to apply during conversion. |
