# Get Original Story with NewsBlur

Retrieves a story's original webpage from NewsBlur.

## Endpoint

- **Method:** `GET`
- **Path:** `/rss_feeds/original_story`
- **Base URL:** `https://www.newsblur.com`
- **Official documentation:** [Get Original Story](https://newsblur.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `story_hash` | query | `string` | yes | Story hash to fetch the original website story for. |
