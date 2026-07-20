# Send WhatsApp Document Message with Sozuri (Kenya) SMS

Sends a WhatsApp document message through Sozuri.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging`
- **Base URL:** `https://sozuri.net/api/v1`
- **Official documentation:** [Send WhatsApp Document Message](https://sozuri.net/docs/whatsapp)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | The WhatsApp business phone number or sender configured in your Sozuri project. |
| `campaign` | body | `string` | no | The campaign name for this message. |
| `to` | body | `string` | yes | The recipient phone number. |
| `document` | body | `object` | yes | The WhatsApp document payload object, including a publicly accessible link and optional filename/caption. |
