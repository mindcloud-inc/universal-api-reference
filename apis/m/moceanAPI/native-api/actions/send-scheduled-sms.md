# Send Scheduled SMS with Mocean API

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/2/sms?mocean-resp-format=json`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [Send Scheduled SMS](https://moceanapi.com/docs#send-sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mocean-from` | query | `string` | yes | SMS sender ID. |
| `mocean-schedule` | query | `string` | yes | Malaysia time schedule in YYYY-MM-DD hh:mm:ss format. |
| `mocean-text` | query | `string` | yes | SMS message text. |
| `mocean-to` | query | `string` | yes | Recipient phone number with country code. |
