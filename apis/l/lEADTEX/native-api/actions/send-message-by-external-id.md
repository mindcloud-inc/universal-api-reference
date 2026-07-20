# Send Message By External ID with LEADTEX

Sends a text message in LEADTEX by external contact ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/sendMessage?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Send Message By External ID](https://docs.leadteh.ru/rabota-s-api/soobsheniya/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_id` | query | `number` | yes | ID of the bot associated with the contact. |
| `contact_external_id` | query | `string` | yes | Phone number or external messenger/social ID for the contact. |
| `messenger` | query | `string` | yes | Messenger identifier such as whatsapp, telegram, viber, or icq. |
| `text` | query | `string` | yes | Message text to send. |
