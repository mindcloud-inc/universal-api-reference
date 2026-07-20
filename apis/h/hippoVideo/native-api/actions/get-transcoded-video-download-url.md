# Get Transcoded Video Download URL with Hippo Video

Retrieves a download URL for a transcoded Hippo Video archive.

## Endpoint

- **Method:** `POST`
- **Path:** `/video/transcoded/signed_url`
- **Base URL:** `https://www.hippovideo.io`
- **Official documentation:** [Get Transcoded Video Download URL](https://help.hippovideo.io/support/solutions/articles/19000158930-transcoded-video-download-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_token` | body | `string` | yes | Unique video token |
