# List Generated Videos by Campaign with BHuman

Retrieves generated videos for a campaign in BHuman.

## Endpoint

- **Method:** `GET`
- **Path:** `/ai_studio/generated_video_by_campaign_id`
- **Base URL:** `https://studio.bhuman.ai/api`
- **Official documentation:** [List Generated Videos by Campaign](https://github.com/bhuman-ai/public_api#api-endpoints)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | query | `string` | yes | The campaign ID to look up generated videos for. |
