# Stop App Preview with Codemagic

Deletes an existing app preview from Codemagic.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v3/previews/:preview_id`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Stop App Preview](https://codemagic.io/api/v3/schema#tag/App%20Previews/operation/ApiV3PreviewsPreviewIdStopPreview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `preview_id` | path | `string` | yes | Codemagic app preview identifier. |
