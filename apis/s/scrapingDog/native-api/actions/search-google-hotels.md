# Search Google Hotels with ScrapingDog

Retrieves Google Hotels search results through ScrapingDog.

## Endpoint

- **Method:** `GET`
- **Path:** `/google_hotels`
- **Base URL:** `https://api.scrapingdog.com`
- **Official documentation:** [Search Google Hotels](https://docs.scrapingdog.com/google-hotels-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `check_in_date` | query | `string` | yes | Check-in date in YYYY-MM-DD format. |
| `check_out_date` | query | `string` | yes | Check-out date in YYYY-MM-DD format. |
| `query` | query | `string` | yes | Search query for Google Hotels. |
