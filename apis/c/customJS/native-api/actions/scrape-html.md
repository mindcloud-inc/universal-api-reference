# Scrape HTML with CustomJS

Retrieves HTML content from a website using CustomJS.

## Endpoint

- **Method:** `POST`
- **Path:** `https://e.customjs.io/scraper`
- **Base URL:** `https://e.customjs.io`
- **API:** rest
- **Official documentation:** [Scrape HTML](https://www.customjs.space/integration/native-api/html-scraper/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input.url` | body | `string` | yes | Website URL to scrape. |
