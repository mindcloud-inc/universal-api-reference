# Replace Background And Relight with Stability AI

Updates an image in Stability AI with background replacement.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/edit/replace-background-and-relight`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Replace Background And Relight](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1replace-background-and-relight/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject_image` | body | `file` | yes | Subject image file to place into the new background and lighting context. |
| `background_prompt` | body | `string` | no | Text prompt describing the desired generated background. Provide this when not using a background reference image. |
