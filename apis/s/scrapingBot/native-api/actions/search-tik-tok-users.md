# Search TikTok Users with ScrapingBot

## Endpoint

- **Method:** `POST`
- **Path:** `/tiktok`
- **Base URL:** `https://scrapingbot.io/api/v1`
- **Official documentation:** [Search TikTok Users](https://scraping-bot.io/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | body | `string` | yes | Keyword to search for users. |
| `count` | body | `number` | no | Number of users to return. |
