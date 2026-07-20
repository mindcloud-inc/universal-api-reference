# Mark WhatsApp Message as Read with D7 Messaging

Marks a WhatsApp message as read in D7 Messaging.

## Endpoint

- **Method:** `POST`
- **Path:** `/whatsapp/v2/read-receipt/:message_id`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Mark WhatsApp Message as Read](https://d7networks.com/docs/whatsapp/read-receipt/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_id` | path | `string` | yes | Message ID to mark as read. |
