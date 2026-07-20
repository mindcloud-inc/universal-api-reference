# Send SMS To Many Numbers with VoiceShot

Creates SMS messages in VoiceShot for many recipients.

## Endpoint

- **Method:** `POST`
- **Path:** `/ivrapi.asp`
- **Base URL:** `https://api.voiceshot.com`
- **Official documentation:** [Send SMS To Many Numbers](https://secure.voiceshot.com/docs/ivrapiv5/txt.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `menuId` | body | `string` | yes | VoiceShot campaign identifier. |
| `callerId` | body | `string` | yes | Caller ID to display for all recipients. |
| `message` | body | `string` | yes | SMS body to send for every recipient. |
| `recipients[]` | body | `array<object>` | yes | Recipient list for the outbound text message. |
| `recipients[].number` | body | `string` | yes | Destination phone number. |
| `recipients[].callId` | body | `string` | no | Optional client-defined call identifier. |
| `recipients[].countryCode` | body | `string` | no | Optional country code. |
| `recipients[].dateAndTime` | body | `string` | no | Optional scheduled delivery time. |
