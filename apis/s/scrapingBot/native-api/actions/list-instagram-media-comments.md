# List Instagram Media Comments with ScrapingBot

## Endpoint

- **Method:** `POST`
- **Path:** `/instagram`
- **Base URL:** `https://scrapingbot.io/api/v1`
- **Official documentation:** [List Instagram Media Comments](https://scraping-bot.io/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | body | `number` | no | Number of comments to return. |
| `media_id` | body | `string` | yes | Instagram media ID. |
