# Get Scraped Paste Raw Data with Pastebin

Retrieves raw data for a scraped Pastebin paste.

## Endpoint

- **Method:** `GET`
- **Path:** `https://scrape.pastebin.com/api_scrape_item.php`
- **Base URL:** `https://pastebin.com/api`
- **Official documentation:** [Get Scraped Paste Raw Data](https://pastebin.com/doc_scraping_api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `i` | query | `string` | yes | The public paste key to fetch through the scraping API. |
