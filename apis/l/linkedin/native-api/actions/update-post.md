# Update Post with LinkedIn

Updates an existing post in LinkedIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/posts/:encodedPostUrn`
- **Base URL:** `https://api.linkedin.com`
- **Official documentation:** [Update Post](https://learn.microsoft.com/en-us/linkedin/marketing/community-management/shares/posts-api?view=li-lms-2025-11)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `encodedPostUrn` | path | `string` | yes | Percent-encoded post URN path segment. |
| `patch` | body | `object` | yes | Partial update patch object, for example {"$set": {...}}. |
