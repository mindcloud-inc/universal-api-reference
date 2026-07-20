# Scrape URL With PATCH with ScrapingAnt

## Endpoint

- **Method:** `PATCH`
- **Path:** `/general`
- **Base URL:** `https://api.scrapingant.com/v2`
- **Official documentation:** [Scrape URL With PATCH](https://docs.scrapingant.com/post-put-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | Fully qualified URL to scrape with a forwarded PATCH request. |
| `body` | body | `string` | no | Body data to forward with the PATCH request when the target URL expects a request body. |
