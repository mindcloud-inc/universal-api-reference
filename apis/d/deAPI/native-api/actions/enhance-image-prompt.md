# Enhance Image Prompt with deAPI

Enhances a text-to-image prompt in deAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/client/prompt/image`
- **Base URL:** `https://api.deapi.ai`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `negative_prompt` | body | `string` | no | Optional negative prompt to preserve and refine. |
| `prompt` | body | `string` | no | Image-generation prompt to enhance. |
