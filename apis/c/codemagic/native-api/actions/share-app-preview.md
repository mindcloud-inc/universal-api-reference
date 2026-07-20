# Share App Preview with Codemagic

Creates a shared link for a Codemagic app preview.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/previews/:preview_id/share`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Share App Preview](https://codemagic.io/api/v3/schema#tag/App%20Previews/operation/ApiV3PreviewsPreviewIdShareSharePreview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `preview_id` | path | `string` | yes | Codemagic app preview identifier. |
