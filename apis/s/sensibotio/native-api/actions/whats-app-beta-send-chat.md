# WhatsApp beta Send Chat with Sensibot.io

Sends a WhatsApp beta chat message through Sensibot.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/whatsappbeta/send`
- **Base URL:** `https://api.sensibot.io`
- **Official documentation:** [WhatsApp beta Send Chat](https://api.sensibot.io/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `is_group` | body | `string` | no |
| `message` | body | `string` | no |
| `recipient` | body | `string` | no |
| `type` | body | `string` | no |
| `wa_number` | body | `string` | no |
