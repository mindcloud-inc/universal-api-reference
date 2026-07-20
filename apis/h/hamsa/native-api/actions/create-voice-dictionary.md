# Create Voice Dictionary with Hamsa

Creates a new voice dictionary in Hamsa.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/voice-agents/voice-dictionaries`
- **Base URL:** `https://api.tryhamsa.com`
- **Official documentation:** [Create Voice Dictionary](https://docs.tryhamsa.com/api-reference/endpoint/create-voice-dictionary)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `words[]` | body | `array<object>` | yes |
| `words[].pronunciation` | body | `string` | yes |
| `words[].pronunciation` | body | `string` | yes |
| `words[].word` | body | `string` | yes |
| `words[].word` | body | `string` | yes |
