# Generate Bulk Personalized Video Tracking IDs with Hippo Video

Creates bulk personalized video tracking IDs in Hippo Video.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/me/video/bulk_personalize`
- **Base URL:** `https://www.hippovideo.io`
- **Official documentation:** [Generate Bulk Personalized Video Tracking IDs](https://help.hippovideo.io/support/solutions/articles/19000099793-bulk-video-personalization-and-tracking-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_id` | body | `number` | yes | ID of the video |
| `file` | body | `string` | yes | Excel, CSV, or XLSX file with customer data |
