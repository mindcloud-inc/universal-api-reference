# Search TikTok Videos with ScrapingBot

## Endpoint

- **Method:** `POST`
- **Path:** `/tiktok`
- **Base URL:** `https://scrapingbot.io/api/v1`
- **Official documentation:** [Search TikTok Videos](https://scraping-bot.io/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | body | `string` | yes | Keyword to search for videos. |
| `count` | body | `number` | no | Number of videos to return. |
