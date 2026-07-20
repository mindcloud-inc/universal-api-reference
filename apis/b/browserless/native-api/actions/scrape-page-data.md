# Scrape Page Data with Browserless

Retrieves structured page data from Browserless using selectors.

## Endpoint

- **Method:** `POST`
- **Path:** `/scrape`
- **Base URL:** `https://production-sfo.browserless.io`
- **Official documentation:** [Scrape Page Data](https://docs.browserless.io/rest-apis/scrape)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The URL to scrape for structured data extraction. |
| `elements[]` | body | `array<object>` | yes | Array of selector objects that define the data to extract. |
