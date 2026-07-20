# Stream Speech File with Hume AI

Streams synthesized speech from Hume AI as an audio file.

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/tts/stream/file`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Stream Speech File](https://dev.hume.ai/reference/text-to-speech-tts/synthesize-file-streaming)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `*/*` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `utterances[0].text` | body | `string` | yes |
| `utterances[0].voice.name` | body | `string` | no |
| `utterances[0].voice.provider` | body | `string` | no |
| `utterances[0].description` | body | `string` | no |
