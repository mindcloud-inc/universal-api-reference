# List Voices with AiVOOV

Retrieves available voice IDs from AiVOOV.

## Endpoint

- **Method:** `GET`
- **Path:** `/voices`
- **Base URL:** `https://aivoov.com/api/v8`
- **Official documentation:** [List Voices](https://github.com/AiVOOV/aivoov-api#get-all-voice-ids)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_code` | query | `string` | no | Filter voices by language code, for example en-US. |
