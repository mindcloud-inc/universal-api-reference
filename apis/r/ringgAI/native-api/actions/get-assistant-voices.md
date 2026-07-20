# Get Assistant Voices with Ringg AI

Retrieves assistant voices from Ringg AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/agent/voices`
- **Base URL:** `https://prod-api.ringg.ai/ca/api/v0`
- **Official documentation:** [Get Assistant Voices](https://docs.ringg.ai/api-reference/endpoint/assistant/get-assistant-voices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language` | query | `string` | no | Filter voices by language (e.g., 'en-US', 'hi-IN'). Multiple languages can be comma-separated. |
