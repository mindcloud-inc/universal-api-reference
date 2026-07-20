# Create Async Batch Jobs with ScraperAPI

Creates async batch scraping jobs in ScraperAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `https://async.scraperapi.com/batchjobs`
- **Base URL:** `https://api.scraperapi.com`
- **Official documentation:** [Create Async Batch Jobs](https://docs.scraperapi.com/asynchronous-api/batch-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urls[]` | body | `array<string>` | yes | The list of target URLs to submit as async jobs. |
