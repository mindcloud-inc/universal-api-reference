# Run YouTube Search Scraper with Botster

Creates a Botster YouTube search extraction job.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/youtube-search-scraper`
- **Base URL:** `https://botster.io/api/v2`
- **Official documentation:** [Run YouTube Search Scraper](https://botster.io/bots/youtube-search-scraper)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Search query. |
| `limit` | body | `string` | yes | How many videos to scrape. |
