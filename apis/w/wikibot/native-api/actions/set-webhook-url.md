# Set Webhook URL with Wikibot

Updates the webhook URL in Wikibot.

## Endpoint

- **Method:** `POST`
- **Path:** `/bot/set-webhook-url`
- **Base URL:** `https://api.wikibot.pro/api`
- **Official documentation:** [Set Webhook URL](https://wikibot.pro/docs/api/set-webhook-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Webhook URL to call for asynchronous results. |
