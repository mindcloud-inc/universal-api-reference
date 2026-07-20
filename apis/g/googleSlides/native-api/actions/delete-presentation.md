# Delete Presentation with Google Slides

Deletes an existing presentation file from Google Slides.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://www.googleapis.com/drive/v3/files/:fileId`
- **Base URL:** `https://slides.googleapis.com`
- **Official documentation:** [Delete Presentation](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `string` | yes | The ID of the presentation file to delete. |
