# Ask Question With Query Parameters with Wikibot

Retrieves a bot answer from Wikibot with query parameters.

## Endpoint

- **Method:** `GET`
- **Path:** `/bot/ask`
- **Base URL:** `https://api.wikibot.pro/api`
- **Official documentation:** [Ask Question With Query Parameters](https://wikibot.pro/docs/api/ask-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | query | `string` | yes | External identifier for the customer chat. |
| `query` | query | `string` | yes | Question or message to send to Wikibot. |
| `format` | query | `list` | no | Answer formatting mode. Accepted values: `0`, `1`. |
| `msgId` | query | `string` | no | Message identifier. |
