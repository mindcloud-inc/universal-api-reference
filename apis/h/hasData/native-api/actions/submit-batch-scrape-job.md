# Submit Batch Scrape Job with HasData

Submits a batch web scrape job to HasData.

## Endpoint

- **Method:** `POST`
- **Path:** `/scrape/batch/web`
- **Base URL:** `https://api.hasdata.com`
- **Official documentation:** [Submit Batch Scrape Job](https://docs.hasdata.com/apis/web-scraping-api/batch-scrape)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requests[].aiExtractRules` | body | `object` | no | Structured extraction schema for this batch item. |
| `requests[].outputFormat[]` | body | `array<string>` | no | Formats to return for this batch item. |
| `requests[].url` | body | `string` | yes | Public URL to scrape for this batch item. |
