# Send Binary SMS with Mocean API

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/2/sms?mocean-resp-format=json&mocean-coding=2`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [Send Binary SMS](https://moceanapi.com/docs#send-sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mocean-from` | query | `string` | yes | SMS sender ID. |
| `mocean-text` | query | `string` | yes | Hex-encoded SMS payload. |
| `mocean-to` | query | `string` | yes | Recipient phone number with country code. |
| `mocean-udh` | query | `string` | no | Optional user data header hex string. |
