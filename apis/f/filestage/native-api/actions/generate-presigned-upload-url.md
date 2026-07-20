# Generate Presigned Upload URL with Filestage

Creates a presigned upload URL in Filestage.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/upload-url`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Generate Presigned Upload URL](https://developers.filestage.io/docs/api/dxto43ie83w98-generate-presigned-upload-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stepId` | body | `string` | no | The ID of the step to upload the file to. This field is required when the `projectId` field is empty |
| `projectId` | body | `string` | no | The ID of the project to upload the file to. This field is required when the `stepId` field is empty |
| `pregenerateFileId` | body | `boolean` | no | When this flag is set to true it generates the ID of the file before it's being uploaded. The `fileId` which is being pre-generated is used as `pregeneratedFileId field in the `POST /files` endpoint.. |
