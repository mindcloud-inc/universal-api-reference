# Get Upload Metadata with FTrack

Retrieves upload metadata from FTrack.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `{serverUrl}`
- **Official documentation:** [Get Upload Metadata](https://developer.ftrack.com/api/operations/get-upload-metadata-api-get-upload-metadata-getuploadmetadata-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `component_id` | body | `string` | yes | Component identifier to upload into. |
