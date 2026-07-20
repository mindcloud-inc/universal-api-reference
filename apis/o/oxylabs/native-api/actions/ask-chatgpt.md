# Ask ChatGPT with Oxylabs

Retrieves ChatGPT prompt responses with Oxylabs.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/queries`
- **Base URL:** `https://realtime.oxylabs.io`
- **Official documentation:** [Ask ChatGPT](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/chatgpt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Prompt to submit to ChatGPT. |
