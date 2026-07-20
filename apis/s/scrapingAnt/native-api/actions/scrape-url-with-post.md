# Scrape URL With POST with ScrapingAnt

Scrapes a URL with a forwarded POST request in ScrapingAnt.

## Endpoint

- **Method:** `POST`
- **Path:** `/general`
- **Base URL:** `https://api.scrapingant.com/v2`
- **Official documentation:** [Scrape URL With POST](https://docs.scrapingant.com/post-put-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | Fully qualified URL to scrape with a forwarded POST request. |
| `body` | body | `string` | no | Body data to forward with the POST request when the target URL expects a request body. |
