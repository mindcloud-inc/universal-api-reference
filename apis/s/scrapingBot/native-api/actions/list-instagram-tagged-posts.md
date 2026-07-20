# List Instagram Tagged Posts with ScrapingBot

## Endpoint

- **Method:** `POST`
- **Path:** `/instagram`
- **Base URL:** `https://scrapingbot.io/api/v1`
- **Official documentation:** [List Instagram Tagged Posts](https://scraping-bot.io/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | body | `number` | no | Number of tagged posts to return. |
| `user_id` | body | `string` | yes | Instagram user ID. |
