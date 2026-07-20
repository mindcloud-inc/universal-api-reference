# List Creator Content Posts with Influencers.club

Retrieves recent creator posts from Influencers.club by platform and handle.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/creators/content/posts/`
- **Base URL:** `https://api-dashboard.influencers.club`
- **Official documentation:** [List Creator Content Posts](https://docs.influencers.club/openapi/creator-posts/public_v1_creators_content_posts_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `platform` | body | `string` | yes | Creator platform (for example instagram). |
| `handle` | body | `string` | yes | Creator handle without @. |
