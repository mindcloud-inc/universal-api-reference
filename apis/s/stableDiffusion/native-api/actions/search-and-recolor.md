# Search And Recolor with Stable Diffusion

Recolors matched content in an image in Stable Diffusion.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/edit/search-and-recolor`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Search And Recolor](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1search-and-recolor/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `string` | yes | Source image to edit. |
| `prompt` | body | `string` | yes | Text prompt describing the recolored output. |
| `select_prompt` | body | `string` | yes | Text describing the region or object to recolor. |
