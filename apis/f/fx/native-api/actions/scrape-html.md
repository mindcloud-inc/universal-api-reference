# Scrape HTML with 1001fx

Retrieves structured content from HTML or a website.

## Endpoint

- **Method:** `POST`
- **Path:** `/data/scrapehtml`
- **Base URL:** `https://api.1001fx.com`
- **Official documentation:** [Scrape HTML](https://1001fx.com/functions/scrapehtml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | no | HTML source to scrape. |
| `selectors[]` | body | `array<object>` | yes | Selectors that define what content to extract. |
| `url` | body | `string` | no | URL to scrape when not passing raw HTML. |
