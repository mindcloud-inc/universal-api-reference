# Update Pixel Event with TikTok Conversions

Updates a Pixel event definition in TikTok Conversions.

## Endpoint

- **Method:** `POST`
- **Path:** `/open_api/v1.3/pixel/event/update/`
- **Base URL:** `https://business-api.tiktok.com`
- **Official documentation:** [Update Pixel Event](https://business-api.tiktok.com/portal/docs?id=1740858823774210)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `advertiser_id` | body | `string` | yes |
| `event_id` | body | `string` | yes |
| `event_name` | body | `string` | yes |
| `currency` | body | `string` | no |
| `currency_value` | body | `number` | no |
