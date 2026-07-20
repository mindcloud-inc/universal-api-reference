# Synthesize Speech JSON with Hume AI

Synthesizes speech in Hume AI and returns JSON audio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/tts`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Synthesize Speech JSON](https://dev.hume.ai/reference/text-to-speech-tts/synthesize-json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format.type` | body | `string` | no | Audio format type. |
| `num_generations` | body | `string` | no | Number of generations to produce. |
| `utterances[0].text` | body | `string` | yes | Text to synthesize. |
| `utterances[0].voice.name` | body | `string` | no | Voice name. |
| `utterances[0].voice.provider` | body | `string` | no | Voice provider. |
| `utterances[0].description` | body | `string` | no | Delivery description for the utterance. |
