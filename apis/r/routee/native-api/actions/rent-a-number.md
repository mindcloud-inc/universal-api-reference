# Rent a Number with Routee

Rents a new number in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/numbers/my`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Rent a Number](https://docs.routee.net/reference/rent-a-number)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msisdn` | body | `string` | yes | The phone number. Format with a '+' and country code e.g., +3069485xxxxx (E.164 format). |
| `inboundSmsCallbackUrl` | body | `string` | no | Defines the callback URL that will receive the inbound messages. |
| `voiceInboundStrategy` | body | `object` | no | Defines the Voice inbound strategy |
| `voiceInboundStrategy.dialplanUrl` | body | `string` | no | Defines the dialplan URL |
| `voiceInboundStrategy.forwardCallToSip` | body | `string` | no | A valid SIP address to forward the inbound call |
| `voiceInboundStrategy.forwardCallTo` | body | `string` | no | A valid phone number in E.164 Format to forward the inbound call |
| `inboundVoiceCallbackUrl` | body | `string` | no | Defines the callback URL that will receive the inbound Voice messages. |
