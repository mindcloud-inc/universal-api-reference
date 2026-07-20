# Crawl Website Main Content with LLMLayer

Streams crawled main website content from LLMLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/crawl_stream`
- **Base URL:** `https://api.llmlayer.dev`
- **Official documentation:** [Crawl Website Main Content](https://docs.llmlayer.ai/api-reference/endpoint/crawl)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Website URL to crawl. |
