# Delete Post with LinkedIn

Deletes an existing post from LinkedIn.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rest/posts/:encodedPostUrn`
- **Base URL:** `https://api.linkedin.com`
- **Official documentation:** [Delete Post](https://learn.microsoft.com/en-us/linkedin/marketing/community-management/shares/posts-api?view=li-lms-2025-11)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `encodedPostUrn` | path | `string` | yes | Percent-encoded post URN path segment. |
