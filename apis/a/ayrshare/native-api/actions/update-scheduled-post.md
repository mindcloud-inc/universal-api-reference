# Update Scheduled Post with Ayrshare

Updates a scheduled post in Ayrshare.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/post`
- **Base URL:** `https://api.ayrshare.com/api`
- **Official documentation:** [Update Scheduled Post](https://www.ayrshare.com/docs/apis/post/update-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Ayrshare scheduled post ID to update. |
| `scheduleDate` | body | `date` | no | New UTC ISO 8601 schedule date for the pending scheduled post. |
| `scheduledPause` | body | `boolean` | no | Pause or unpause a scheduled post. |
