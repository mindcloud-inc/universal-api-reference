# Get App Preview with Codemagic

Retrieves a specific app preview from Codemagic.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/previews/:preview_id`
- **Base URL:** `https://codemagic.io`
- **Official documentation:** [Get App Preview](https://codemagic.io/api/v3/schema#tag/App%20Previews/operation/ApiV3PreviewsPreviewIdGetPreviewInformation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `preview_id` | path | `string` | yes | Codemagic app preview identifier. |
