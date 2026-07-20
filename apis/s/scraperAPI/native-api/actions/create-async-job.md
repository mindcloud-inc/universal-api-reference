# Create Async Job with ScraperAPI

Creates an async scraping job in ScraperAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `https://async.scraperapi.com/jobs`
- **Base URL:** `https://api.scraperapi.com`
- **Official documentation:** [Create Async Job](https://docs.scraperapi.com/asynchronous-api/job-handling)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | Optional request body to forward to the target URL. |
| `headers` | body | `object` | no | Optional target request headers. |
| `meta` | body | `object` | no | Optional metadata returned with the async job. |
| `method` | body | `string` | no | Optional HTTP method for the target request. |
| `url` | body | `string` | yes | The target URL to scrape asynchronously. |
