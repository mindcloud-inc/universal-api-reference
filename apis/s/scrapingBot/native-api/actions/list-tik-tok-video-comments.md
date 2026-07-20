# List TikTok Video Comments with ScrapingBot

## Endpoint

- **Method:** `POST`
- **Path:** `/tiktok`
- **Base URL:** `https://scrapingbot.io/api/v1`
- **Official documentation:** [List TikTok Video Comments](https://scraping-bot.io/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aweme_id` | body | `string` | yes | TikTok video ID. |
| `count` | body | `number` | no | Number of comments to return. |
