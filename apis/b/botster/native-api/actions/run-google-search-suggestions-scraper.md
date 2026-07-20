# Run Google Search Suggestions Scraper with Botster

Creates a Botster Google search suggestions job.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/google-search-suggestions-scraper`
- **Base URL:** `https://botster.io/api/v2`
- **Official documentation:** [Run Google Search Suggestions Scraper](https://botster.io/bots/google-search-suggestions-scraper)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Seed keywords. |
| `region_key` | body | `string` | yes | Region. |
| `region_lang` | body | `string` | yes | Language. |
| `providers[]` | body | `array<string>` | no | Additional search engines to extract suggestions from. |
| `depth` | body | `list` | yes | Search depth. Accepted values: `Depth 1`, `Depth 2`, `Depth 3`. |
| `append[]` | body | `array<string>` | yes | Methods for expanding the query. |
