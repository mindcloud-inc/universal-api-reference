# Send Bulk SMS with Mocean API

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/2/sms?mocean-resp-format=json`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [Send Bulk SMS](https://moceanapi.com/docs#send-sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mocean-from` | query | `string` | yes | SMS sender ID. |
| `mocean-text` | query | `string` | yes | SMS message text sent to every recipient. |
| `mocean-to` | query | `string` | yes | Recipient numbers separated by spaces or commas. |
