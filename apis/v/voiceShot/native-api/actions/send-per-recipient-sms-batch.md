# Send Per-Recipient SMS Batch with VoiceShot

Creates per-recipient SMS messages in VoiceShot.

## Endpoint

- **Method:** `POST`
- **Path:** `/ivrapi.asp`
- **Base URL:** `https://api.voiceshot.com`
- **Official documentation:** [Send Per-Recipient SMS Batch](https://secure.voiceshot.com/docs/ivrapiv5/txt.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `menuId` | body | `string` | yes | VoiceShot campaign identifier. |
| `recipients[]` | body | `array<object>` | yes | Recipient list with per-recipient SMS content. |
| `recipients[].number` | body | `string` | yes | Destination phone number. |
| `recipients[].message` | body | `string` | yes | SMS body for this recipient. |
| `recipients[].callId` | body | `string` | no | Optional client-defined call identifier. |
| `recipients[].callerId` | body | `string` | no | Optional caller ID for this recipient. |
| `recipients[].countryCode` | body | `string` | no | Optional country code. |
| `recipients[].dateAndTime` | body | `string` | no | Optional scheduled delivery time. |
