# Replace Background And Relight with Stable Diffusion

Replaces an image background and relights the subject in Stable Diffusion.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/edit/replace-background-and-relight`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Replace Background And Relight](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1replace-background-and-relight/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject_image` | body | `string` | yes | Foreground subject image to relight against a generated or referenced background. |
