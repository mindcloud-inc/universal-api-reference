# Send Voice Blast with Nvoip

## Endpoint

- **Method:** `POST`
- **Path:** `/torpedo/voice`
- **Base URL:** `https://api.nvoip.com.br/v2`
- **Official documentation:** [Send Voice Blast](https://github.com/Nvoip/nvoip-integrationAPI/blob/main/torpedo.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audio` | body | `string` | yes | Audio file URL or identifier used in the voice message. |
| `audios[]` | body | `array<object>` | yes | Array of audio instructions. |
| `called` | body | `string` | yes | Destino da chamada de voz. |
| `caller` | body | `string` | yes | Origem da chamada de voz. |
| `positionAudio` | body | `number` | yes | Playback order for the audio item. |
