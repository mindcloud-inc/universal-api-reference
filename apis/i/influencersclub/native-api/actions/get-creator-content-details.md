# Get Creator Content Details with Influencers.club

Retrieves detailed metrics for specific creator content in Influencers.club.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/creators/content/details/`
- **Base URL:** `https://api-dashboard.influencers.club`
- **Official documentation:** [Get Creator Content Details](https://docs.influencers.club/openapi/post-details/public_v1_creators_content_details_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `platform` | body | `string` | yes | Platform of the content (instagram, tiktok, youtube). |
| `content_type` | body | `string` | yes | Content details to fetch (data, comments, transcript, audio). |
| `post_id` | body | `string` | yes | Target platform post identifier. |
| `pagination_token` | body | `string` | no | Token for next comment page. |
