# Scrape URL With DELETE with ScrapingAnt

Scrapes a URL with a forwarded DELETE request in ScrapingAnt.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/general`
- **Base URL:** `https://api.scrapingant.com/v2`
- **Official documentation:** [Scrape URL With DELETE](https://docs.scrapingant.com/post-put-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | Fully qualified URL to scrape with a forwarded DELETE request. |
| `body` | body | `string` | no | Body data to forward with the DELETE request when the target URL expects a request body. |
