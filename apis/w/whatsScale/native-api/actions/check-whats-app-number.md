# Check WhatsApp Number with WhatsScale

Checks whether a phone number uses WhatsApp via WhatsScale.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/checkWhatsapp`
- **Base URL:** `https://proxy.whatsscale.com`
- **Official documentation:** [Check WhatsApp Number](https://whatsscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | body | `string` | yes | Phone number to check. |
| `session` | body | `string` | yes | Session name from /api/sessions. |
