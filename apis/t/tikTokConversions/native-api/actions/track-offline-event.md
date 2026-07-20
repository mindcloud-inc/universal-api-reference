# Track Offline Event with TikTok Conversions

Reports an offline event to TikTok Conversions.

## Endpoint

- **Method:** `POST`
- **Path:** `/open_api/v1.3/offline/track/`
- **Base URL:** `https://business-api.tiktok.com`
- **Official documentation:** [Track Offline Event](https://business-api.tiktok.com/portal/docs?id=1758428013689857)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `event_set_id` | body | `string` | yes |
| `event` | body | `string` | yes |
| `event_id` | body | `string` | no |
| `timestamp` | body | `number` | yes |
| `context.user.emails[]` | body | `array<string>` | no |
| `context.user.phone_numbers[]` | body | `array<string>` | no |
| `properties.order_id` | body | `string` | no |
| `properties.shop_id` | body | `string` | no |
| `properties.currency` | body | `string` | no |
| `properties.value` | body | `number` | no |
| `properties.event_channel` | body | `string` | no |
| `properties.contents[].content_id` | body | `string` | no |
| `properties.contents[].quantity` | body | `number` | no |
| `properties.contents[].price` | body | `number` | no |
