# Synthesize speech with Hume

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/tts`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Synthesize speech](https://dev.hume.ai/reference/text-to-speech-tts/synthesize-json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `utterances[]` | body | `array<object>` | yes | Array of utterances to synthesize. |
| `format` | body | `object` | no | Optional output audio format object, for example {"type":"mp3"}. |
| `split_utterances` | body | `boolean` | no | Whether to split utterances into natural-sounding segments. |
| `num_generations` | body | `number` | no | Number of generations to produce. |
