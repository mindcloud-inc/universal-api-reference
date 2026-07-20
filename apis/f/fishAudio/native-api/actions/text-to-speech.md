# Text to Speech with Fish Audio

Converts text to speech with Fish Audio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tts`
- **Base URL:** `https://api.fish.audio`
- **Official documentation:** [Text to Speech](https://docs.fish.audio/api-reference/endpoint/openapi-v1/text-to-speech)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text to synthesize. |
| `reference_id` | body | `string` | no | Optional model ID or speaker reference ID. |
| `format` | body | `list` | no | Output audio format. Accepted values: `0`, `1`, `2`. |
| `sample_rate` | body | `number` | no | Output sample rate. |
| `mp3_bitrate` | body | `number` | no | MP3 bitrate when format is mp3. |
| `normalize` | body | `boolean` | no | Normalize the generated audio. |
| `temperature` | body | `number` | no | Sampling temperature. |
| `top_p` | body | `number` | no | Top-p sampling value. |
