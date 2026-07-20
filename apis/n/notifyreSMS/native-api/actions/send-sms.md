# Send SMS with Notifyre SMS

Creates an SMS message in Notifyre.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/send`
- **Base URL:** `https://api.notifyre.com/20220711`
- **Official documentation:** [Send SMS](https://docs.notifyre.com/api/sms-send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | SMS message body. |
| `campaignName` | body | `string` | no | Optional campaign label. |
| `from` | body | `string` | yes | Sending number or sender ID. |
| `recipients` | body | `list<string>` | yes | Recipient phone numbers. |
