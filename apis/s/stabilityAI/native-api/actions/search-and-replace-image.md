# Search And Replace Image with Stability AI

Updates an image in Stability AI by search and replace.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/edit/search-and-replace`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Search And Replace Image](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1search-and-replace/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Source image file to edit. |
| `prompt` | body | `string` | yes | Replacement prompt describing what should appear. |
| `search_prompt` | body | `string` | yes | Description of the object or region to search for and replace. |
