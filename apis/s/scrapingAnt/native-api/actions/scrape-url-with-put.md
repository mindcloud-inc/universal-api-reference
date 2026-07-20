# Scrape URL With PUT with ScrapingAnt

Scrapes a URL with a forwarded PUT request in ScrapingAnt.

## Endpoint

- **Method:** `PUT`
- **Path:** `/general`
- **Base URL:** `https://api.scrapingant.com/v2`
- **Official documentation:** [Scrape URL With PUT](https://docs.scrapingant.com/post-put-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | Fully qualified URL to scrape with a forwarded PUT request. |
| `body` | body | `string` | no | Body data to forward with the PUT request when the target URL expects a request body. |
