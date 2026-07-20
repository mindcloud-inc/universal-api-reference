# Send SMS Message with TeleSign

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messaging`
- **Base URL:** `https://rest-ww.telesign.com`
- **Official documentation:** [Send SMS Message](https://developer.telesign.com/enterprise/reference/sendsms)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `phone_number` | body | `string` | yes |
| `message` | body | `string` | yes |
| `message_type` | body | `string` | yes |
| `account_lifecycle_event` | body | `string` | no |
| `originating_ip` | body | `string` | no |
| `external_id` | body | `string` | no |
