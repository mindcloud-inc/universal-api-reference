# Convert Text to Speech with VoiceRSS (Independent Publisher)

Creates speech audio from text in VoiceRSS.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://api.voicerss.org`
- **Official documentation:** [Convert Text to Speech](https://www.voicerss.org/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hl` | query | `string` | yes | Text language code, such as `en-us`. |
| `src` | query | `string` | yes | Text to convert to speech. VoiceRSS limits this to 100KB. Maximum length: 100000. |
| `v` | query | `string` | no | Optional VoiceRSS voice name. Default depends on the selected language. |
| `r` | query | `number` | no | Speech rate from -10 through 10. Default is 0. |
| `c` | query | `list<string>` | no | Audio codec. Defaults to WAV when omitted. Accepted values: `0`, `1`, `2`, `3`, `4`. |
| `f` | query | `string` | no | Audio format. Defaults to 8khz_8bit_mono when omitted. |
| `ssml` | query | `boolean` | no | Whether source text uses SSML format. |
| `b64` | query | `boolean` | no | Return audio as a Base64 string instead of binary audio data. |
