# Upload Files with Anchor

Uploads files to a browser session in Anchor.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sessions/:sessionId/uploads`
- **Base URL:** `https://api.anchorbrowser.io`
- **Official documentation:** [Upload Files](https://docs.anchorbrowser.io/api-reference/browser-sessions/upload-files)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
| `sessionId` | path | `string` | yes |
