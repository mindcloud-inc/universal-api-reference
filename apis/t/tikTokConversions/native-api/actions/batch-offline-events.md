# Batch Offline Events with TikTok Conversions

Reports offline events in bulk to TikTok Conversions.

## Endpoint

- **Method:** `POST`
- **Path:** `/open_api/v1.3/offline/batch/`
- **Base URL:** `https://business-api.tiktok.com`
- **Official documentation:** [Batch Offline Events](https://business-api.tiktok.com/portal/docs?id=1758428053652482)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `event_set_id` | body | `string` | yes |
| `batch[].event` | body | `string` | yes |
| `batch[].event_id` | body | `string` | no |
| `batch[].timestamp` | body | `number` | yes |
| `batch[].context.user.emails[]` | body | `array<string>` | no |
| `batch[].context.user.phone_numbers[]` | body | `array<string>` | no |
| `batch[].properties.order_id` | body | `string` | no |
| `batch[].properties.shop_id` | body | `string` | no |
| `batch[].properties.currency` | body | `string` | no |
| `batch[].properties.value` | body | `number` | no |
| `batch[].properties.event_channel` | body | `string` | no |
| `batch[].properties.contents[].content_id` | body | `string` | no |
| `batch[].properties.contents[].quantity` | body | `number` | no |
| `batch[].properties.contents[].price` | body | `number` | no |
