# Send SMS with SMS8.io

## Endpoint

- **Method:** `GET`
- **Path:** `send.php`
- **Base URL:** `https://app.sms8.io/services`
- **Official documentation:** [Send SMS](https://sms8.io/sms8-api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | query | `string` | yes | Recipient phone number. |
| `message` | query | `string` | yes | SMS body text (URL-encoded by the platform). |
| `devices` | query | `string` | yes | JSON-encoded array of devices and SIM slots, for example ["182\|0","182\|1"]. |
| `prioritize` | query | `number` | no | Prioritize device for sending when multiple devices are available. |
