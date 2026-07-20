# Set Envelope Notification with Sign.Plus

## Endpoint

- **Method:** `PUT`
- **Path:** `/envelope/:envelope_id/set_notification`
- **Base URL:** `https://restapi.sign.plus/v2`
- **Official documentation:** [Set Envelope Notification](https://apidoc.sign.plus/api-reference/endpoints/signplus/set-envelope-notification)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `envelope_id` | path | `string` | yes |
| `subject` | body | `string` | yes |
| `message` | body | `string` | yes |
| `reminder_interval` | body | `number` | yes |
