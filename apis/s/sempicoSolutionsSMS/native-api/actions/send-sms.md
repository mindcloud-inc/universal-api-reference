# Send SMS with Sempico Solutions SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/send`
- **Base URL:** `https://restapi.sempico.solutions/v1`
- **Official documentation:** [Send SMS](https://restapi.gatum.io/desc/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number[]` | body | `array<string>` | yes | Destination phone numbers in MSISDN format. |
| `senderID` | body | `string` | yes | Registered sender ID from which the SMS will be sent. Sempico rejects unregistered sender IDs with not_registr_originator. |
| `text` | body | `string` | yes | SMS message text. |
| `type` | body | `list` | no | Message type. Sempico documents sms, hlr, and mnp; defaults to sms. Accepted values: `0`, `1`, `2`. |
| `beginDate` | body | `date` | no | Date when the message should be sent, in YYYY-MM-DD format. |
| `beginTime` | body | `string` | no | GMT+0 time when the message should be sent, in HH:MM:SS format. |
| `lifetime` | body | `number` | no | How many seconds the SMS should live before expiring. |
| `delivery` | body | `boolean` | no | Whether Sempico should return delivery report information. |
