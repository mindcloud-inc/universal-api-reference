# Create Style Check with Markup AI

Creates a style check in Markup AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/style/checks`
- **Base URL:** `https://api.markup.ai`
- **Official documentation:** [Create Style Check](https://docs.markup.ai/api-reference/style-checks/create-style-check)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dialect` | body | `string` | yes | The language variant to use for analysis. |
| `tone` | body | `string` | no | Optional tone variation to target. |
| `style_guide` | body | `string` | yes | Style guide ID or built-in preset such as ap, chicago, or microsoft. |
| `webhook_url` | body | `string` | no | Optional URL to receive the completed workflow result. |
| `file_upload` | body | `file` | yes | The document to analyze. |
