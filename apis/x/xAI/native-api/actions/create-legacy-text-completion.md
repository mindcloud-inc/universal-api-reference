# Create Legacy Text Completion with xAI

Creates a legacy text completion in the xAI API.

## Endpoint

- **Method:** `POST`
- **Path:** `/completions`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [Create Legacy Text Completion](https://docs.x.ai/developers/rest-api-reference/inference/legacy#create-text-completion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | no | Model name to use for the legacy text completion. |
| `prompt` | body | `string` | no | Text prompt for the completion. |
| `max_tokens` | body | `number` | no | Maximum number of generated tokens. |
