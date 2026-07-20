# Search Google Lens with ScrapingDog

Retrieves Google Lens results through ScrapingDog.

## Endpoint

- **Method:** `GET`
- **Path:** `/google_lens`
- **Base URL:** `https://api.scrapingdog.com`
- **Official documentation:** [Search Google Lens](https://docs.scrapingdog.com/google-lens-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | Google Lens URL, typically a lens.google.com upload-by-url link. |
