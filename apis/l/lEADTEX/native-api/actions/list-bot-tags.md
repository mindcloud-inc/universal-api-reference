# List Bot Tags with LEADTEX

Retrieves tags for a specific bot in LEADTEX.

## Endpoint

- **Method:** `GET`
- **Path:** `/getBotTags?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [List Bot Tags](https://docs.leadteh.ru/rabota-s-api/kontakty/tegi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_id` | query | `number` | yes | ID of the bot whose tags should be returned. |
