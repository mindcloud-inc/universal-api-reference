# Download File with Localazy

Retrieves a translated file from Localazy.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/files/:fileId/download/:lang`
- **Base URL:** `https://api.localazy.com`
- **Official documentation:** [Download File](https://localazy.com/docs/api/files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Localazy project id. |
| `fileId` | path | `string` | yes | Localazy file id. |
| `lang` | path | `string` | yes | Locale code to download. |
