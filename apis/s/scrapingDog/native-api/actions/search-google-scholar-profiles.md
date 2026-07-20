# Search Google Scholar Profiles with ScrapingDog

Retrieves Google Scholar profiles through ScrapingDog.

## Endpoint

- **Method:** `GET`
- **Path:** `/google_scholar/profiles`
- **Base URL:** `https://api.scrapingdog.com`
- **Official documentation:** [Search Google Scholar Profiles](https://docs.scrapingdog.com/google-scholar-api/google-scholar-profiles-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mauthors` | query | `string` | yes | Author name or query string to look up Google Scholar profiles. |
