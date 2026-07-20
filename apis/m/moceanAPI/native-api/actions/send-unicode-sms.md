# Send Unicode SMS with Mocean API

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/2/sms?mocean-resp-format=json&mocean-charset=UTF-8`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [Send Unicode SMS](https://moceanapi.com/docs#send-sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mocean-from` | query | `string` | yes | SMS sender ID. |
| `mocean-text` | query | `string` | yes | Unicode SMS message text. |
| `mocean-to` | query | `string` | yes | Recipient phone number with country code. |
