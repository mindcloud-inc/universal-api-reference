# Create Offline Event Set with TikTok Conversions

Creates a new Offline Event set in TikTok Conversions.

## Endpoint

- **Method:** `POST`
- **Path:** `/open_api/v1.3/offline/create/`
- **Base URL:** `https://business-api.tiktok.com`
- **Official documentation:** [Create Offline Event Set](https://business-api.tiktok.com/portal/docs?id=1758427576470529)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `advertiser_id` | body | `string` | yes |
| `name` | body | `string` | yes |
| `auto_tracking` | body | `boolean` | no |
