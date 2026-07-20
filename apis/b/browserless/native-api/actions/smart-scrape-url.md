# Smart Scrape Url with Browserless

Retrieves structured page data from a URL in Browserless.

## Endpoint

- **Method:** `POST`
- **Path:** `/smart-scrape`
- **Base URL:** `https://production-sfo.browserless.io`
- **Official documentation:** [Smart Scrape Url](https://docs.browserless.io/rest-apis/smart-scrape)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The URL to scrape. Must be an http or https URL. |
| `formats[]` | body | `array<string>` | no | Optional output formats to include in the smart scrape response. |
| `timeout` | query | `number` | no | Optional timeout in milliseconds for the smart scrape request. |
