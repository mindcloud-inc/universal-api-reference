# List TikTok Music Posts with ScrapingBot

## Endpoint

- **Method:** `POST`
- **Path:** `/tiktok`
- **Base URL:** `https://scrapingbot.io/api/v1`
- **Official documentation:** [List TikTok Music Posts](https://scraping-bot.io/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `music_id` | body | `string` | yes | TikTok music or sound ID. |
| `count` | body | `number` | no | Number of videos to return. |
