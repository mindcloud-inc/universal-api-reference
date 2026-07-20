# Improve Prompt with Freepik

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/ai/improve-prompt`
- **Base URL:** `https://api.freepik.com`
- **Official documentation:** [Improve Prompt](https://docs.freepik.com/api-reference/improve-prompt/enhance-prompt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Prompt text to improve. |
| `type` | body | `list` | yes | Prompt type to improve: image or video. Accepted values: `image`, `video`. |
| `language` | body | `string` | no | Two-letter output language code. |
