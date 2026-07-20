# Generate Text to Speech Route with Hamsa

Generates text-to-speech output in Hamsa.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/jobs/text-to-speech`
- **Base URL:** `https://api.tryhamsa.com`
- **Official documentation:** [Generate Text to Speech Route](https://docs.tryhamsa.com/api-reference/endpoint/generate-text-to-speech)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `text` | body | `string` | yes |
| `voiceId` | body | `string` | yes |
| `voiceId` | body | `string` | yes |
| `webhookAuth` | body | `object` | no |
| `webhookUrl` | body | `string` | no |
