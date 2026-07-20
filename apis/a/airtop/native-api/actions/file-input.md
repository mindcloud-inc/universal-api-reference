# File Input with Airtop

Uploads a file in a specific Airtop window.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions/:sessionId/windows/:windowId/file-input`
- **Base URL:** `https://api.airtop.ai/api/v1`
- **Official documentation:** [File Input](https://docs.airtop.ai/api-reference/airtop-api/windows/file-input)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sessionId` | path | `string` | yes |
| `windowId` | path | `string` | yes |
| `fileId` | body | `string` | no |
| `fileName` | body | `string` | no |
| `elementDescription` | body | `string` | no |
