# List TikTok User Videos with ScrapingBot

## Endpoint

- **Method:** `POST`
- **Path:** `/tiktok`
- **Base URL:** `https://scrapingbot.io/api/v1`
- **Official documentation:** [List TikTok User Videos](https://scraping-bot.io/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `unique_id` | body | `string` | yes | TikTok username without @. |
| `count` | body | `number` | no | Number of videos to return. |
