# Get Page Source with ScrapeUnblocker

Retrieves page source from ScrapeUnblocker.

## Endpoint

- **Method:** `POST`
- **Path:** `/getPageSource`
- **Base URL:** `https://scrapeunblocker.p.rapidapi.com`
- **Official documentation:** [Get Page Source](https://www.scrapeunblocker.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The webpage URL to fetch. |
| `proxy_country` | query | `string` | no | Optional proxy country code. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. |
