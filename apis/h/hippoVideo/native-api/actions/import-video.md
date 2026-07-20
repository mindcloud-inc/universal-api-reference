# Import Video with Hippo Video

Imports a video into Hippo Video from a downloadable URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/me/video/import`
- **Base URL:** `https://www.hippovideo.io`
- **Official documentation:** [Import Video](https://help.hippovideo.io/support/solutions/articles/19000100703-import-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Video title |
| `URL` | body | `string` | yes | Downloadable URL of the video |
