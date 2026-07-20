# Get Viewer Profile by Lead Email with Hippo Video

Retrieves viewer profiles in Hippo Video by lead email.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/me/video/viewer_profile`
- **Base URL:** `https://www.hippovideo.io`
- **Official documentation:** [Get Viewer Profile by Lead Email](https://help.hippovideo.io/support/solutions/articles/19000095984-video-reports-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_email` | query | `string` | yes | Email address of the lead |
