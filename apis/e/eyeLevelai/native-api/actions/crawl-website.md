# Crawl Website with EyeLevel.ai

Crawls a website into EyeLevel.ai for ingestion.

## Endpoint

- **Method:** `POST`
- **Path:** `/ingest/documents/website`
- **Base URL:** `https://api.groundx.ai/api/v1`
- **Official documentation:** [Crawl Website](https://docs.eyelevel.ai/reference/api-reference/documents/crawl-website)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `websites` | body | `list<object>` | yes | An array of website crawl definitions to ingest. |
