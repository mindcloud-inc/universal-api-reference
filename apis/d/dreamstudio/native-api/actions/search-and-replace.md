# Search and Replace with Dreamstudio

Replaces a selected object in an image in Dreamstudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/edit/search-and-replace`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Search and Replace](https://platform.stability.ai/docs/api-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Image file to edit. |
| `prompt` | body | `string` | yes | Prompt describing the replacement result. |
| `search_prompt` | body | `string` | yes | Text describing which object or region should be replaced. |
