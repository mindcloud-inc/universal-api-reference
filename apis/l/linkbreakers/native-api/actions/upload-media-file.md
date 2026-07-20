# Upload a Media File with Linkbreakers

Uploads a media file to Linkbreakers.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/media`
- **Base URL:** `https://api.linkbreakers.com`
- **Official documentation:** [Upload a Media File](https://linkbreakers.com/help/api/media)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileData` | body | `string` | no | The base64-encoded file data to upload. |
| `fileName` | body | `string` | no | The name of the file. |
| `mediaType` | body | `string` | no | The type of media being uploaded. |
| `visibility` | body | `string` | no | The visibility of the uploaded media. |
