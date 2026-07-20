# Update Offline Event Set with TikTok Conversions

Updates an existing Offline Event set in TikTok Conversions.

## Endpoint

- **Method:** `POST`
- **Path:** `/open_api/v1.3/offline/update/`
- **Base URL:** `https://business-api.tiktok.com`
- **Official documentation:** [Update Offline Event Set](https://business-api.tiktok.com/portal/docs?id=1765596741157889)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `advertiser_id` | body | `string` | yes |
| `event_set_id` | body | `string` | yes |
| `name` | body | `string` | no |
| `auto_tracking` | body | `boolean` | no |
