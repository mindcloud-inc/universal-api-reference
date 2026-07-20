# Create Scrape with Olostep

Creates a new scrape in Olostep.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/scrapes`
- **Base URL:** `https://api.olostep.com`
- **Official documentation:** [Create Scrape](https://docs.olostep.com/api-reference/scrapes/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url_to_scrape` | body | `string` | yes | The URL to start scraping from. |
| `formats[]` | body | `array<string>` | no | Optional formats in which to return content. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. Send multiple values as a array. |
