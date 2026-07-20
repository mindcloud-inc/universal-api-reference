# Enhance Prompt with APImage

Rewrites a prompt for AI image generation in APImage.

## Endpoint

- **Method:** `POST`
- **Path:** `https://app.apimage.org/api/v1/image-studio`
- **Base URL:** `https://apimage.org/api`
- **Official documentation:** [Enhance Prompt](https://apimage.org/docs/api-reference#enhance-prompt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Prompt to rewrite into a more descriptive image-generation prompt. |
