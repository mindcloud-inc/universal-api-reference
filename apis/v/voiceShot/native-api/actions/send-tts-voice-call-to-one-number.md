# Send TTS Voice Call To One Number with VoiceShot

Creates a TTS voice call in VoiceShot.

## Endpoint

- **Method:** `POST`
- **Path:** `/ivrapi.asp`
- **Base URL:** `https://api.voiceshot.com`
- **Official documentation:** [Send TTS Voice Call To One Number](https://secure.voiceshot.com/docs/ivrapiv5/tts.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `menuId` | body | `string` | yes | VoiceShot campaign identifier. |
| `callerId` | body | `string` | yes | Caller ID to display for the outbound call. |
| `number` | body | `string` | yes | Destination phone number. |
| `promptId` | body | `string` | yes | Prompt identifier inside the VoiceShot campaign. |
| `message` | body | `string` | yes | Text-to-speech message to speak. |
| `callId` | body | `string` | no | Optional client-defined call identifier. |
| `countryCode` | body | `string` | no | Optional country code for the destination number. |
| `dateAndTime` | body | `string` | no | Optional scheduled delivery time. |
| `transferTo` | body | `string` | no | Optional phone number to transfer the recipient to. |
