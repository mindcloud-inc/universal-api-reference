# Compare Creator Audience Overlap with Influencers.club

Retrieves audience overlap metrics for multiple creators in Influencers.club.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/creators/audience/overlap/`
- **Base URL:** `https://api-dashboard.influencers.club`
- **Official documentation:** [Compare Creator Audience Overlap](https://docs.influencers.club/openapi/audience-overlap/public_v1_creators_audience_overlap_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `platform` | body | `string` | yes | Platform to compare (instagram, tiktok, youtube). |
| `creators[]` | body | `array<string>` | yes | Array of 2-10 creator usernames or profile URLs. |
