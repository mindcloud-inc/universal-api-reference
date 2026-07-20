# WhatsApp Cloud Send Message with Sensibot.io

Sends a WhatsApp Cloud message through Sensibot.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/whatsappcloud/send`
- **Base URL:** `https://api.sensibot.io`
- **Official documentation:** [WhatsApp Cloud Send Message](https://api.sensibot.io/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cloud_wa_number` | body | `string` | no |
| `message` | body | `string` | no |
| `recipient` | body | `string` | no |
| `type` | body | `string` | no |
