# List Videos with Hippo Video

Retrieves videos from the Hippo Video library.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/me/videos/list`
- **Base URL:** `https://www.hippovideo.io`
- **Official documentation:** [List Videos](https://help.hippovideo.io/support/solutions/articles/19000095981-video-library-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | yes | Page number of the list |
| `category_id` | query | `number` | no | ID of the category or folder |
| `video_type` | query | `string` | no | Type of video such as library or testimonial |
