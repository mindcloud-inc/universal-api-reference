# Send SMS To One Number with VoiceShot

Creates an SMS message in VoiceShot.

## Endpoint

- **Method:** `POST`
- **Path:** `/ivrapi.asp`
- **Base URL:** `https://api.voiceshot.com`
- **Official documentation:** [Send SMS To One Number](https://secure.voiceshot.com/docs/ivrapiv5/txt.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `menuId` | body | `string` | yes | VoiceShot campaign identifier. |
| `callerId` | body | `string` | yes | Caller ID to display for the outbound text. |
| `number` | body | `string` | yes | Destination phone number. |
| `message` | body | `string` | yes | SMS body to send. |
| `callId` | body | `string` | no | Optional client-defined call identifier. |
| `countryCode` | body | `string` | no | Optional country code for the destination number. |
| `dateAndTime` | body | `string` | no | Optional scheduled delivery time. |
