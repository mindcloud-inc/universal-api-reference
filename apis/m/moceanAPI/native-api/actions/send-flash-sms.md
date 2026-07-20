# Send Flash SMS with Mocean API

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/2/sms?mocean-resp-format=json&mocean-mclass=1&mocean-alt-dcs=1`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [Send Flash SMS](https://moceanapi.com/docs#send-sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mocean-from` | query | `string` | yes | SMS sender ID. |
| `mocean-text` | query | `string` | yes | Flash SMS message text. |
| `mocean-to` | query | `string` | yes | Recipient phone number with country code. |
