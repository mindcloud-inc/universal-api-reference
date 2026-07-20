# Run Google Maps Places Scraper with Botster

Creates a Botster Google Maps place extraction job.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/google-maps-places-scraper`
- **Base URL:** `https://botster.io/api/v2`
- **Official documentation:** [Run Google Maps Places Scraper](https://botster.io/bots/google-maps-places-scraper)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `coordinates` | body | `object` | yes | Location coordinates and zoom level for the Google Maps search origin. |
| `depth` | body | `string` | yes | How deep the Maps search should go. |
| `input` | body | `string` | yes | Google Maps search keywords. |
