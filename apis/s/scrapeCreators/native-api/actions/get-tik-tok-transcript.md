# Get TikTok Transcript with Scrape Creators

Retrieves a TikTok video transcript from Scrape Creators.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/tiktok/video/transcript`
- **Base URL:** `https://api.scrapecreators.com`
- **Official documentation:** [Get TikTok Transcript](https://docs.scrapecreators.com/v1/tiktok/video/transcript/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | TikTok video URL |
| `language` | query | `string` | no | Transcript language |
| `use_ai_as_fallback` | query | `boolean` | no | Use AI if a transcript is not directly available |
