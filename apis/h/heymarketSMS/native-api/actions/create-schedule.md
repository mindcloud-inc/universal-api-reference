# Create Schedule with Heymarket SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/schedule`
- **Base URL:** `https://api.heymarket.com`
- **Official documentation:** [Create Schedule](https://heymarket.docs.apiary.io/api-description-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | body | `number` | yes | Unique identifier for the inbox from which the scheduled message will be sent. |
| `execute_at` | body | `string` | yes | Time at which the message will be sent in RFC 3339 format. |
| `phone_number` | body | `string` | no | Target phone number in E.164 format without the plus sign. |
| `content.text` | body | `string` | yes | Text content of the scheduled message. |
| `content.to` | body | `string` | no | Recipient echoed inside the scheduled content object. |
| `local_id` | body | `string` | no | Client unique identifier for the scheduled message. |
| `user_id` | body | `number` | no | Sender user ID. Defaults to the team owner if omitted. |
