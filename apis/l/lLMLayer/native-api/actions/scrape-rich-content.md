# Scrape Rich Content with LLMLayer

Retrieves scraped markdown with images and links from LLMLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/scrape`
- **Base URL:** `https://api.llmlayer.dev`
- **Official documentation:** [Scrape Rich Content](https://docs.llmlayer.ai/api-reference/endpoint/scrape)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Website URL to scrape. |
