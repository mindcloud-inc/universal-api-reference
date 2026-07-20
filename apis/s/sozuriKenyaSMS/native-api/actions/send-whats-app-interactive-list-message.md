# Send WhatsApp Interactive List Message with Sozuri (Kenya) SMS

Sends a WhatsApp interactive list through Sozuri.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging`
- **Base URL:** `https://sozuri.net/api/v1`
- **Official documentation:** [Send WhatsApp Interactive List Message](https://sozuri.net/docs/whatsapp)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | The WhatsApp business phone number or sender configured in your Sozuri project. |
| `campaign` | body | `string` | no | The campaign name for this message. |
| `to` | body | `string` | yes | The recipient phone number. |
| `interactive` | body | `object` | yes | The WhatsApp interactive payload object for a list message. |
