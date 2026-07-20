# List Voices with Pipio

Finds available voice options in Pipio.

## Endpoint

- **Method:** `GET`
- **Path:** `/voice`
- **Base URL:** `https://avatar.pipio.ai`
- **Official documentation:** [List Voices](https://docs.pipio.ai/voice-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languages` | query | `string` | no | Filter voices by language code. |
| `gender` | query | `list` | no | Filter voices by gender. Accepted values: `female`, `male`. |
| `voiceTypes` | query | `list` | no | Filter voices by voice type. Accepted values: `Character`, `Conversational`, `Narration`, `Promotional`. |
