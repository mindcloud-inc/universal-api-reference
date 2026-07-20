# Get Google Scholar Author Citation with ScrapingDog

Retrieves Google Scholar author citations through ScrapingDog.

## Endpoint

- **Method:** `GET`
- **Path:** `/google_scholar/author`
- **Base URL:** `https://api.scrapingdog.com`
- **Official documentation:** [Get Google Scholar Author Citation](https://docs.scrapingdog.com/google-scholar-api/google-scholar-author-api/google-scholar-author-citation-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `author_id` | query | `string` | yes | Google Scholar author identifier. |
| `citation_id` | query | `string` | yes | Citation identifier returned by the Google Scholar author response. |
