# Get Model with Anthropic

Retrieves a specific model from Anthropic.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/models/:model_id`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [Get Model](https://platform.claude.com/docs/en/api/models/retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model_id` | path | `string` | yes | The model ID. |
