# Get YouTube Transcript with Scrape Creators

Retrieves a YouTube video transcript from Scrape Creators.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/youtube/video/transcript`
- **Base URL:** `https://api.scrapecreators.com`
- **Official documentation:** [Get YouTube Transcript](https://docs.scrapecreators.com/v1/youtube/video/transcript/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | YouTube video URL |
| `language` | query | `string` | no | Transcript language |
