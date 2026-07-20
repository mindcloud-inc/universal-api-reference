# Run Google Search Scraper with Botster

Creates a Botster Google search results extraction job.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/google-snippet-scraper`
- **Base URL:** `https://botster.io/api/v2`
- **Official documentation:** [Run Google Search Scraper](https://botster.io/bots/google-snippet-scraper)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Search keywords and phrases. |
| `device` | body | `list` | yes | Target device type. Accepted values: `Desktop`, `Mobile`. |
| `language` | body | `string` | yes | ISO 639-1 two-letter language code. |
| `coordinates` | body | `object` | yes | Location coordinates and zoom level for geo-specific results. |
| `os` | body | `list` | yes | Operating system for the selected device type. Accepted values: `Android`, `Windows`, `iOS`, `macOS`. |
| `depth` | body | `list` | yes | How many search results to extract. Accepted values: `First Organic Result`, `Top 10`, `Top 100`, `Top 20`, `Top 200`, `Top 50`, `Top 500`. |
| `cron` | body | `string` | no | Cron expression for periodic runs. |
| `new_items_only` | body | `boolean` | no | Return only items that appeared since the latest crawl. |
