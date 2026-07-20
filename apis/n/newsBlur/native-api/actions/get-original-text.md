# Get Original Text with NewsBlur

Retrieves a story's original text from NewsBlur.

## Endpoint

- **Method:** `GET`
- **Path:** `/rss_feeds/original_text`
- **Base URL:** `https://www.newsblur.com`
- **Official documentation:** [Get Original Text](https://newsblur.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `story_hash` | query | `string` | yes | Story hash to fetch extracted full text for. |
