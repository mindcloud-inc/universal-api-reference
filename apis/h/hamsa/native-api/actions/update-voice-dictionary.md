# Update Voice Dictionary with Hamsa

Updates an existing voice dictionary in Hamsa.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/voice-agents/voice-dictionaries/:voiceDictionaryId`
- **Base URL:** `https://api.tryhamsa.com`
- **Official documentation:** [Update Voice Dictionary](https://docs.tryhamsa.com/api-reference/endpoint/update-voice-dictionary)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | yes |
| `words[]` | body | `array<object>` | yes |
| `words[].pronunciation` | body | `string` | yes |
| `words[].pronunciation` | body | `string` | yes |
| `words[].word` | body | `string` | yes |
| `words[].word` | body | `string` | yes |
