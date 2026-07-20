# Fetch And Parse Url With Custom Parser with ScrapeOps

Fetches and parses a URL with a ScrapeOps custom parser.

## Endpoint

- **Method:** `GET`
- **Path:** `https://proxy.scrapeops.io/v1/`
- **Base URL:** `http://headers.scrapeops.io/v1`
- **Official documentation:** [Fetch And Parse Url With Custom Parser](https://scrapeops.io/docs/parser-api/custom-parser/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The URL to fetch and parse with the selected custom parser. |
| `custom_parser_id` | query | `string` | yes | The ScrapeOps custom parser ID created in the ScrapeOps app. |
| `render_js` | query | `boolean` | no | Enable JavaScript rendering for the target page before parsing. |
