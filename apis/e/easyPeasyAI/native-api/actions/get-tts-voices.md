# Get TTS Voices with Easy-Peasy.AI

Retrieves TTS voices from Easy-Peasy.AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/get-text-to-speech-voices`
- **Base URL:** `https://easy-peasy.ai`
- **API:** rest
- **Official documentation:** [Get TTS Voices](https://docs.easy-peasy.ai/api-reference/endpoint/get-tts-voices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accent` | query | `string` | no | Optional accent used to filter voices. |
| `include_custom` | query | `boolean` | no | Include account-specific custom voices in the response when available. |
| `language` | query | `string` | no | Optional language code used to filter voices. |
