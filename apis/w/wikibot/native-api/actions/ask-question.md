# Ask Question with Wikibot

Creates a bot answer in Wikibot.

## Endpoint

- **Method:** `POST`
- **Path:** `/bot/ask`
- **Base URL:** `https://api.wikibot.pro/api`
- **Official documentation:** [Ask Question](https://wikibot.pro/docs/api/ask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | body | `string` | yes | External identifier for the customer chat. |
| `query` | body | `string` | yes | Question or message to send to Wikibot. |
| `format` | body | `list` | no | Answer formatting mode. Accepted values: `0`, `1`. |
| `msgId` | body | `string` | no | Message identifier. |
| `attachments[]` | body | `array<string>` | no | Attachment URLs to include with the question. Send multiple values as a array. |
| `agentId` | body | `number` | no | Identifier of the agent that should handle the request. |
