# Ask Perplexity with Oxylabs

Retrieves Perplexity prompt responses with Oxylabs.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/queries`
- **Base URL:** `https://realtime.oxylabs.io`
- **Official documentation:** [Ask Perplexity](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/perplexity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Prompt to submit to Perplexity. |
