# Create Response with xAI

Creates a response in the xAI API.

## Endpoint

- **Method:** `POST`
- **Path:** `/responses`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [Create Response](https://docs.x.ai/developers/rest-api-reference/inference/chat#create-new-response)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | no | Input text or structured input messages for the response. |
| `model` | body | `string` | no | Model name to use for the response. |
| `max_output_tokens` | body | `number` | no | Maximum output tokens for the response. |
| `store` | body | `boolean` | no | Whether xAI stores the response for later retrieval. |
