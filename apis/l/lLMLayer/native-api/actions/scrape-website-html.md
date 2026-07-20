# Scrape Website HTML with LLMLayer

Retrieves scraped website content as HTML from LLMLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/scrape`
- **Base URL:** `https://api.llmlayer.dev`
- **Official documentation:** [Scrape Website HTML](https://docs.llmlayer.ai/api-reference/endpoint/scrape)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Website URL to scrape. |
