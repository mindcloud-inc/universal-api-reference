# Upload Video by URL (Mapped Field) with ZapCap

Uploads a video to ZapCap from a public URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/videos/url`
- **Base URL:** `https://api.zapcap.ai`
- **Official documentation:** [Upload Video by URL (Mapped Field)](https://platform.zapcap.ai/docs/api#tag/videos/post/videos/url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Publicly accessible MP4 URL to import into ZapCap. |
