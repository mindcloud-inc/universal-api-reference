# Send Message with Heymarket SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/message/send`
- **Base URL:** `https://api.heymarket.com`
- **Official documentation:** [Send Message](https://heymarket.docs.apiary.io/api-description-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inbox_id` | body | `number` | yes | Unique identifier for the inbox from which the message will be sent. |
| `creator_id` | body | `number` | yes | Unique identifier for the sender. |
| `phone_number` | body | `string` | no | Target phone number in E.164 format without the plus sign. |
| `text` | body | `string` | no | Message text body. |
| `template_id` | body | `number` | no | Unique identifier of the Heymarket template. |
| `local_id` | body | `string` | no | Client unique identifier for the message. |
| `private` | body | `boolean` | no | Create a private comment within a Heymarket conversation. |
