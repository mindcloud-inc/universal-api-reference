# Get TikTok Video Info with Scrape Creators

Retrieves TikTok video details from Scrape Creators.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/tiktok/video`
- **Base URL:** `https://api.scrapecreators.com`
- **Official documentation:** [Get TikTok Video Info](https://docs.scrapecreators.com/v2/tiktok/video/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | TikTok video URL |
| `get_transcript` | query | `boolean` | no | Include transcript in the video response when supported |
| `region` | query | `string` | no | Proxy region |
| `trim` | query | `boolean` | no | Return a trimmed response |
