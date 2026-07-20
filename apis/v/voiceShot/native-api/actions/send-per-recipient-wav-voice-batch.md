# Send Per-Recipient WAV Voice Batch with VoiceShot

Creates per-recipient WAV voice calls in VoiceShot.

## Endpoint

- **Method:** `POST`
- **Path:** `/ivrapi.asp`
- **Base URL:** `https://api.voiceshot.com`
- **Official documentation:** [Send Per-Recipient WAV Voice Batch](https://secure.voiceshot.com/docs/ivrapiv5/outboundposts.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `menuId` | body | `string` | yes | VoiceShot campaign identifier. |
| `callerId` | body | `string` | no | Optional default caller ID when a recipient does not provide one. |
| `promptId` | body | `string` | yes | Prompt identifier inside the VoiceShot campaign. |
| `recipients[]` | body | `array<object>` | yes | Recipient list with per-recipient WAV prompts. |
| `recipients[].number` | body | `string` | yes | Destination phone number. |
| `recipients[].filename` | body | `string` | yes | Previously uploaded WAV file to play for this recipient. |
| `recipients[].callId` | body | `string` | no | Optional client-defined call identifier. |
| `recipients[].callerId` | body | `string` | no | Optional caller ID override. |
| `recipients[].countryCode` | body | `string` | no | Optional country code. |
| `recipients[].dateAndTime` | body | `string` | no | Optional scheduled delivery time. |
| `recipients[].transferTo` | body | `string` | no | Optional transfer target for this recipient. |
