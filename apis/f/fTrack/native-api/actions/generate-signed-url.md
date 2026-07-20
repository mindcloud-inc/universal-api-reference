# Generate Signed URL with FTrack

Generates a signed URL in FTrack.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `{serverUrl}`
- **Official documentation:** [Generate Signed URL](https://developer.ftrack.com/api/operations/generate-signed-url-api-generate-signed-url-generatesignedurl-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_type` | body | `string` | yes | Entity type for the component or entity. |
| `entity_key` | body | `string` | yes | Key or id identifying the entity. |
