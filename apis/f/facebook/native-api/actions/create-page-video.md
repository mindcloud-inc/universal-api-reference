# Create Page Video with Facebook

## Endpoint

- **Method:** `POST`
- **Path:** `/:pageId/videos`
- **Base URL:** `https://graph.facebook.com/v25.0`
- **Official documentation:** [Create Page Video](https://developers.facebook.com/docs/graph-api/reference/page/videos/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `list<string>` | yes | — |
| `file_url` | body | `string` | yes | Publicly accessible URL of the video file. |
| `title` | body | `string` | no | — |
| `description` | body | `string` | no | Text for the post about the video. |
| `published` | body | `boolean` | no | Set to false to create an unpublished video post. |
| `scheduled_publish_time` | body | `date` | no | 10 minutes to 6 months from now. Set Published to false when scheduling. |
