# Parse Html With Custom Parser with ScrapeOps

Parses HTML with a ScrapeOps custom parser.

## Endpoint

- **Method:** `POST`
- **Path:** `https://parser.scrapeops.io/v1/custom-parser`
- **Base URL:** `http://headers.scrapeops.io/v1`
- **Official documentation:** [Parse Html With Custom Parser](https://scrapeops.io/docs/parser-api/custom-parser/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_parser_id` | query | `string` | yes | The ScrapeOps custom parser ID created in the ScrapeOps app. |
| `html` | body | `string` | yes | The raw HTML to parse with the selected custom parser. |
