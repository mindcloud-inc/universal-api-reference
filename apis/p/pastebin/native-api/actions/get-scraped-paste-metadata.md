# Get Scraped Paste Metadata with Pastebin

Retrieves metadata for a scraped Pastebin paste.

## Endpoint

- **Method:** `GET`
- **Path:** `https://scrape.pastebin.com/api_scrape_item_meta.php`
- **Base URL:** `https://pastebin.com/api`
- **Official documentation:** [Get Scraped Paste Metadata](https://pastebin.com/doc_scraping_api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `i` | query | `string` | yes | The public paste key to inspect through the scraping API metadata endpoint. |
