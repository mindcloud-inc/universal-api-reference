# Send Content with ManyChat

Sends content to a subscriber in ManyChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/fb/sending/sendContent`
- **Base URL:** `https://api.manychat.com`
- **Official documentation:** [Send Content](https://api.manychat.com/swagger#/Sending/b6ae94031676b69a57eb2ad5ea1413f9)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `subscriber_id` | body | `number` | yes |
| `data` | body | `object` | yes |
| `message_tag` | body | `string` | no |
| `otn_topic_name` | body | `string` | no |
