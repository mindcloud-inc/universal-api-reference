# Google Search with ScrapingBot

## Endpoint

- **Method:** `POST`
- **Path:** `/google`
- **Base URL:** `https://scrapingbot.io/api/v1`
- **Official documentation:** [Google Search](https://scraping-bot.io/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | body | `string` | yes | Google search query. |
| `gl` | body | `string` | no | Country code for localized results, such as us or de. |
| `hl` | body | `string` | no | Language code for localized results, such as en or es. |
| `num` | body | `number` | no | Number of search results to return. |
| `page` | body | `number` | no | Page number of the search results. |
