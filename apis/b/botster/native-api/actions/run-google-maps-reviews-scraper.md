# Run Google Maps Reviews Scraper with Botster

Creates a Botster Google review extraction job.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/google-maps-reviews-scraper`
- **Base URL:** `https://botster.io/api/v2`
- **Official documentation:** [Run Google Maps Reviews Scraper](https://botster.io/bots/google-maps-reviews-scraper)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `coordinates` | body | `object` | yes | Location coordinates and zoom level for the Google query origin. |
| `depth` | body | `string` | yes | Number of positions to inspect. |
| `input` | body | `string` | yes | Keywords, place_id, or cid. |
