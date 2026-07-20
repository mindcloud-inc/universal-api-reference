# Update a Number with Routee

Updates an existing number in Routee.

## Endpoint

- **Method:** `PUT`
- **Path:** `/numbers/my/:msisdn`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Update a Number](https://docs.routee.net/reference/update-a-number)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msisdn` | path | `string` | yes | The phone number in E.164 format, without the '+' sign before the country code e.g., 447403940655. |
| `inboundSmsCallbackUrl` | body | `string` | no | Defines the callback URL that will receive the inbound messages. |
| `voiceInboundStrategy` | body | `object` | no | Defines the Voice inbound strategy |
| `voiceInboundStrategy.dialplanUrl` | body | `string` | no | Defines the dialplan URL |
| `inboundVoiceCallbackUrl` | body | `string` | no | Defines the callback URL that will receive the inbound Voice messages. |
