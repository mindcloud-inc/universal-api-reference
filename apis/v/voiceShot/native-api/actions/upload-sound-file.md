# Upload Sound File with VoiceShot

Creates a sound file in VoiceShot.

## Endpoint

- **Method:** `POST`
- **Path:** `/ivrapi.asp`
- **Base URL:** `https://api.voiceshot.com`
- **Official documentation:** [Upload Sound File](https://secure.voiceshot.com/docs/ivrapiv5/uploadingsoundfiles.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | body | `string` | yes | WAV filename to create in VoiceShot. |
| `fileContentBase64` | body | `string` | yes | Base64-encoded WAV file contents. |
