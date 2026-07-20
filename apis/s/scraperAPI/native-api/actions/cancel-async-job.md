# Cancel Async Job with ScraperAPI

Cancels an async scraping job in ScraperAPI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://async.scraperapi.com/jobs/:jobId`
- **Base URL:** `https://api.scraperapi.com`
- **Official documentation:** [Cancel Async Job](https://docs.scraperapi.com/asynchronous-api/job-handling)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The async job ID. |
