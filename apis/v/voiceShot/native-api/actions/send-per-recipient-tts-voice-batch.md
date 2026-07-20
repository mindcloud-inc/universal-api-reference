# Send Per-Recipient TTS Voice Batch with VoiceShot

Creates per-recipient TTS voice calls in VoiceShot.

## Endpoint

- **Method:** `POST`
- **Path:** `/ivrapi.asp`
- **Base URL:** `https://api.voiceshot.com`
- **Official documentation:** [Send Per-Recipient TTS Voice Batch](https://secure.voiceshot.com/docs/ivrapiv5/tts.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `menuId` | body | `string` | yes | VoiceShot campaign identifier. |
| `callerId` | body | `string` | no | Optional default caller ID when a recipient does not provide one. |
| `promptId` | body | `string` | yes | Prompt identifier inside the VoiceShot campaign. |
| `recipients[]` | body | `array<object>` | yes | Recipient list with per-recipient TTS content. |
| `recipients[].number` | body | `string` | yes | Destination phone number. |
| `recipients[].message` | body | `string` | yes | Text-to-speech message to speak for this recipient. |
| `recipients[].callId` | body | `string` | no | Optional client-defined call identifier. |
| `recipients[].callerId` | body | `string` | no | Optional caller ID override. |
| `recipients[].countryCode` | body | `string` | no | Optional country code. |
| `recipients[].dateAndTime` | body | `string` | no | Optional scheduled delivery time. |
| `recipients[].transferTo` | body | `string` | no | Optional transfer target for this recipient. |
