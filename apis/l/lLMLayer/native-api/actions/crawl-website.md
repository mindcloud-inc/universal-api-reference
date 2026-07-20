# Crawl Website with LLMLayer

Streams crawled website pages from LLMLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/crawl_stream`
- **Base URL:** `https://api.llmlayer.dev`
- **Official documentation:** [Crawl Website](https://docs.llmlayer.ai/api-reference/endpoint/crawl)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Website URL to crawl. |
