# Send SMS With Delivery Report with Mocean API

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/2/sms?mocean-resp-format=json&mocean-dlr-mask=1`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [Send SMS With Delivery Report](https://moceanapi.com/docs#send-sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mocean-dlr-url` | query | `string` | no | Webhook URL for delivery reports. |
| `mocean-from` | query | `string` | yes | SMS sender ID. |
| `mocean-text` | query | `string` | yes | SMS message text. |
| `mocean-to` | query | `string` | yes | Recipient phone number with country code. |
