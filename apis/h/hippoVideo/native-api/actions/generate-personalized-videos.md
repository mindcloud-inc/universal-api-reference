# Generate Personalized Videos with Hippo Video

Creates personalized videos in Hippo Video.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/me/video/personalize`
- **Base URL:** `https://www.hippovideo.io`
- **Official documentation:** [Generate Personalized Videos](https://help.hippovideo.io/support/solutions/articles/19000095986-generate-personalized-videos-through-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_id` | body | `number` | yes | ID of the video |
| `merge_fields` | body | `string` | yes | JSON array of merge field values |
