# Replace Background and Relight with Dreamstudio

Replaces an image background and relights it in Dreamstudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/edit/replace-background-and-relight`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Replace Background and Relight](https://platform.stability.ai/docs/api-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject_image` | body | `file` | yes | Foreground subject image used for the background replacement job. |
| `background_prompt` | body | `string` | no | Optional text describing the replacement background. |
