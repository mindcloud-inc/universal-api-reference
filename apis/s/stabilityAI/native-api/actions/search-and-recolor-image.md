# Search And Recolor Image with Stability AI

Updates an image in Stability AI by search and recolor.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/edit/search-and-recolor`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Search And Recolor Image](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1search-and-recolor/post)

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
| `prompt` | body | `string` | yes | Prompt describing the desired color or visual change. |
| `select_prompt` | body | `string` | yes | Description of the object or region to select for recoloring. |
