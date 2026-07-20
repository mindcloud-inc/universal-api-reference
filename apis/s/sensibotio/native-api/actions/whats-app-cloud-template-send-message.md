# WhatsApp Cloud Template Send Message with Sensibot.io

Sends a WhatsApp Cloud template message through Sensibot.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/whatsappcloud/send_template`
- **Base URL:** `https://api.sensibot.io`
- **Official documentation:** [WhatsApp Cloud Template Send Message](https://api.sensibot.io/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cloud_wa_number` | body | `string` | no |
| `recipient` | body | `string` | no |
| `template_language` | body | `string` | no |
| `template_name` | body | `string` | no |
