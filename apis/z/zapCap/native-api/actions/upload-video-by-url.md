# Upload Video By URL with ZapCap

Uploads a video to ZapCap from a public URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/videos/url`
- **Base URL:** `https://api.zapcap.ai`
- **Official documentation:** [Upload Video By URL](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public MP4 URL to import into ZapCap. |
