# Send WAV Voice Call To Many Numbers with VoiceShot

Creates WAV voice calls in VoiceShot for many recipients.

## Endpoint

- **Method:** `POST`
- **Path:** `/ivrapi.asp`
- **Base URL:** `https://api.voiceshot.com`
- **Official documentation:** [Send WAV Voice Call To Many Numbers](https://secure.voiceshot.com/docs/ivrapiv5/filename.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `menuId` | body | `string` | yes | VoiceShot campaign identifier. |
| `callerId` | body | `string` | yes | Caller ID to display for all recipients. |
| `promptId` | body | `string` | yes | Prompt identifier inside the VoiceShot campaign. |
| `filename` | body | `string` | yes | Previously uploaded WAV file to play for every recipient. |
| `transferTo` | body | `string` | no | Optional phone number to transfer recipients to. |
| `recipients[]` | body | `array<object>` | yes | Recipient list for the outbound call. |
| `recipients[].number` | body | `string` | yes | Destination phone number. |
| `recipients[].callId` | body | `string` | no | Optional client-defined call identifier. |
| `recipients[].countryCode` | body | `string` | no | Optional country code. |
| `recipients[].dateAndTime` | body | `string` | no | Optional scheduled delivery time. |
