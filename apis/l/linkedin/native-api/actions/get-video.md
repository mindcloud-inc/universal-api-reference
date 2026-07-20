# Get Video with LinkedIn

Retrieves a video from LinkedIn.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/videos/:videoUrn`
- **Base URL:** `https://api.linkedin.com`
- **Official documentation:** [Get Video](https://learn.microsoft.com/en-us/linkedin/marketing/community-management/shares/videos-api?view=li-lms-2026-02)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoUrn` | path | `string` | yes | Video URN, for example urn:li:video:{id}. |
