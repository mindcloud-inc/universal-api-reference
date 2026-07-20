# Send WhatsApp Message with LEADTEX

Sends a WhatsApp message by phone number in LEADTEX.

## Endpoint

- **Method:** `POST`
- **Path:** `/sendMessageToWhatsApp?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Send WhatsApp Message](https://docs.leadteh.ru/rabota-s-api/soobsheniya/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | body | `string` | yes | WhatsApp phone number. |
| `text` | body | `string` | yes | Message text to send. |
