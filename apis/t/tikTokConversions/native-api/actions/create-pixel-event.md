# Create Pixel Event with TikTok Conversions

Creates a Pixel event definition in TikTok Conversions.

## Endpoint

- **Method:** `POST`
- **Path:** `/open_api/v1.3/pixel/event/create/`
- **Base URL:** `https://business-api.tiktok.com`
- **Official documentation:** [Create Pixel Event](https://business-api.tiktok.com/portal/docs?id=1740858807646209)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `advertiser_id` | body | `string` | yes |
| `pixel_id` | body | `string` | yes |
| `pixel_events[].event_type` | body | `string` | yes |
| `pixel_events[].event_name` | body | `string` | yes |
| `pixel_events[].event_code` | body | `string` | no |
| `pixel_events[].event_id` | body | `string` | no |
| `pixel_events[].currency` | body | `string` | no |
| `pixel_events[].currency_value` | body | `number` | no |
| `pixel_events[].statistic_type` | body | `string` | no |
| `pixel_events[].rules[].trigger` | body | `string` | no |
| `pixel_events[].rules[].operator` | body | `string` | no |
| `pixel_events[].rules[].value` | body | `string` | no |
| `pixel_events[].rules[].variable` | body | `string` | no |
