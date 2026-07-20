# List Instagram User Posts with ScrapingBot

## Endpoint

- **Method:** `POST`
- **Path:** `/instagram`
- **Base URL:** `https://scrapingbot.io/api/v1`
- **Official documentation:** [List Instagram User Posts](https://scraping-bot.io/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | body | `number` | no | Number of posts to return. |
| `user_id` | body | `string` | yes | Instagram user ID. |
