# Send Location with WhatsScale

Sends a location message through WhatsScale.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/sendLocation`
- **Base URL:** `https://proxy.whatsscale.com`
- **Official documentation:** [Send Location](https://whatsscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | body | `string` | yes | Recipient chat ID. |
| `latitude` | body | `number` | yes | Latitude from -90 to 90. |
| `longitude` | body | `number` | yes | Longitude from -180 to 180. |
| `session` | body | `string` | yes | Session name from /api/sessions. |
| `title` | body | `string` | no | Optional label for the location pin. |
