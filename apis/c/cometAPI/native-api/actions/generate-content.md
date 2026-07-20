# Generate Content with CometAPI

Generates content with Gemini models in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1beta/models/:model`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Generate Content](https://www.cometapi.com/how-to-use-ai-api-via-cometapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contents[]` | body | `array<object>` | yes | Gemini contents array. |
| `model` | path | `string` | yes | Gemini model ID. |
