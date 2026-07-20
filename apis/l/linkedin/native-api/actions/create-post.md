# Create Post with LinkedIn

Creates a new post in LinkedIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/posts`
- **Base URL:** `https://api.linkedin.com`
- **Official documentation:** [Create Post](https://learn.microsoft.com/en-us/linkedin/marketing/community-management/shares/posts-api?view=li-lms-2025-11)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `author` | body | `string` | yes | Author URN such as urn:li:organization:{id} or urn:li:person:{id}. |
| `commentary` | body | `string` | yes | Text content for the post commentary. |
| `visibility` | body | `list` | no | Who can see the post. Accepted values: `CONNECTIONS`, `CONTAINER`, `LOGGED_IN`, `PUBLIC`, `TARGETED_ENTITIES`. |
