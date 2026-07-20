# Add Storage with Crowdin

Uploads a file to Crowdin storage.

## Endpoint

- **Method:** `POST`
- **Path:** `/storages`
- **Base URL:** `https://api.crowdin.com/api/v2`
- **Official documentation:** [Add Storage](https://support.crowdin.com/developer/api/v2/#operation/api.storages.post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fileName` | body | `string` | yes |
| `contentType` | body | `string` | no |
| `fileContentBase64` | body | `string` | yes |
