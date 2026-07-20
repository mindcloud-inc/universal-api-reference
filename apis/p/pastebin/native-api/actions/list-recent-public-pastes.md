# List Recent Public Pastes with Pastebin

Retrieves recent public pastes from Pastebin.

## Endpoint

- **Method:** `GET`
- **Path:** `https://scrape.pastebin.com/api_scraping.php`
- **Base URL:** `https://pastebin.com/api`
- **Official documentation:** [List Recent Public Pastes](https://pastebin.com/doc_scraping_api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | Optional number of recent public pastes to return. Pastebin allows up to 250. |
| `lang` | query | `string` | no | Optional syntax filter such as php, javascript, or text. |
