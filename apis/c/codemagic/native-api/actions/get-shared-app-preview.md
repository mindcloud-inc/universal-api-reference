# Get Shared App Preview with Codemagic

Retrieves a shared app preview from Codemagic.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/shared-previews/:shared_preview_id`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Get Shared App Preview](https://codemagic.io/api/v3/schema#tag/App%20Previews/operation/ApiV3SharedPreviewsSharedPreviewIdGetSharedPreview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shared_preview_id` | path | `string` | yes | Codemagic shared preview identifier. |
