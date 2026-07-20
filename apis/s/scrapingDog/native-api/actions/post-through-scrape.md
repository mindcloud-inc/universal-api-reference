# Post Through Scrape with ScrapingDog

Sends a POST request through ScrapingDog.

## Endpoint

- **Method:** `POST`
- **Path:** `/scrape`
- **Base URL:** `https://api.scrapingdog.com`
- **Official documentation:** [Post Through Scrape](https://docs.scrapingdog.com/post-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | Target URL that ScrapingDog should request before sending the POST body. |
