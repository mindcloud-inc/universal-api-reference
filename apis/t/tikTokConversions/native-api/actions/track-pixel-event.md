# Track Pixel Event with TikTok Conversions

Tracks a Pixel event in TikTok Conversions.

## Endpoint

- **Method:** `POST`
- **Path:** `/open_api/v1.3/pixel/track/`
- **Base URL:** `https://business-api.tiktok.com`
- **Official documentation:** [Track Pixel Event](https://business-api.tiktok.com/portal/docs?id=1740858531237890)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `event` | body | `string` | yes |
| `event_id` | body | `string` | no |
| `timestamp` | body | `number` | no |
| `context.ad.callback` | body | `string` | no |
| `context.page.url` | body | `string` | no |
| `context.page.referrer` | body | `string` | no |
| `context.user.external_id` | body | `string` | no |
| `context.user.email` | body | `string` | no |
| `context.user.phone_number` | body | `string` | no |
| `context.user.ttp` | body | `string` | no |
| `context.ip` | body | `string` | no |
| `context.user_agent` | body | `string` | no |
| `properties.content_type` | body | `string` | no |
| `properties.currency` | body | `string` | no |
| `properties.value` | body | `number` | no |
| `properties.query` | body | `string` | no |
| `properties.description` | body | `string` | no |
| `properties.status` | body | `string` | no |
| `properties.contents[].price` | body | `number` | no |
| `properties.contents[].quantity` | body | `number` | no |
| `properties.contents[].content_id` | body | `string` | no |
| `properties.contents[].content_category` | body | `string` | no |
| `properties.contents[].content_name` | body | `string` | no |
| `properties.contents[].brand` | body | `string` | no |
