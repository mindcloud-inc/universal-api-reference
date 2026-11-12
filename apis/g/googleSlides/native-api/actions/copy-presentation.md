# Copy Presentation with Google Slides

Creates a copy of an existing presentation, optionally with a new title.

## Endpoint

- **Method:** `POST`
- **Path:** `/drive/v3/files/:fileId/copy`
- **Base URL:** `https://www.googleapis.com`
- **API:** Google Drive API
- **Official documentation:** [Copy Presentation](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/copy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `list<string>` | yes | The ID of the presentation to copy. |
| `name` | body | `string` | no | Title for the new copy. Google names it "Copy of" the original title when omitted. |
| `description` | body | `string` | no | — |
