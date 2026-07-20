# Connect WhatsApp Number with Wbiztool

Connects a WhatsApp account in Wbiztool.

## Endpoint

- **Method:** `POST`
- **Path:** `/whatsapp/connect/`
- **Base URL:** `https://wbiztool.com/api/v1`
- **Official documentation:** [Connect WhatsApp Number](https://wbiztool.com/docs/whatsapp-connect-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `whatsapp_number` | body | `string` | yes | WhatsApp number to connect, including country code. |
| `webhook_url` | body | `string` | no | Webhook URL to receive events for the connected number. |
