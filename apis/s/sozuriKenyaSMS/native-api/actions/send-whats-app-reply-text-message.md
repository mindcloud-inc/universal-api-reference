# Send WhatsApp Reply Text Message with Sozuri (Kenya) SMS

Sends a WhatsApp reply text message through Sozuri.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging`
- **Base URL:** `https://sozuri.net/api/v1`
- **Official documentation:** [Send WhatsApp Reply Text Message](https://sozuri.net/docs/whatsapp)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | The WhatsApp business phone number or sender configured in your Sozuri project. |
| `campaign` | body | `string` | no | The campaign name for this message. |
| `context` | body | `object` | yes | The WhatsApp reply context object containing the previous message_id. |
| `to` | body | `string` | yes | The recipient phone number. |
| `text` | body | `object` | yes | The WhatsApp text payload object, including the message body and optional preview_url flag. |
