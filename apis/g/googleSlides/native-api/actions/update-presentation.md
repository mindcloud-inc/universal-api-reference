# Update Presentation with Google Slides

Updates an existing presentation file in Google Slides.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://www.googleapis.com/drive/v3/files/:fileId`
- **Base URL:** `https://slides.googleapis.com`
- **Official documentation:** [Update Presentation](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `string` | yes | The ID of the presentation file to update. |
| `name` | body | `string` | yes | The new file name for the presentation. |
