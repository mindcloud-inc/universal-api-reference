# Batch Pixel Events with TikTok Conversions

Tracks Pixel events in bulk in TikTok Conversions.

## Endpoint

- **Method:** `POST`
- **Path:** `/open_api/v1.3/pixel/batch/`
- **Base URL:** `https://business-api.tiktok.com`
- **Official documentation:** [Batch Pixel Events](https://business-api.tiktok.com/portal/docs?id=1740858565852225)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `batch[].event` | body | `string` | yes |
| `batch[].event_id` | body | `string` | no |
| `batch[].timestamp` | body | `number` | no |
| `batch[].context.ad.callback` | body | `string` | no |
| `batch[].context.page.url` | body | `string` | no |
| `batch[].context.page.referrer` | body | `string` | no |
| `batch[].context.user.external_id` | body | `string` | no |
| `batch[].context.user.email` | body | `string` | no |
| `batch[].context.user.phone_number` | body | `string` | no |
| `batch[].context.user.ttp` | body | `string` | no |
| `batch[].context.ip` | body | `string` | no |
| `batch[].context.user_agent` | body | `string` | no |
| `batch[].properties.content_type` | body | `string` | no |
| `batch[].properties.currency` | body | `string` | no |
| `batch[].properties.value` | body | `number` | no |
| `batch[].properties.query` | body | `string` | no |
| `batch[].properties.description` | body | `string` | no |
| `batch[].properties.status` | body | `string` | no |
| `batch[].properties.contents[].price` | body | `number` | no |
| `batch[].properties.contents[].quantity` | body | `number` | no |
| `batch[].properties.contents[].content_id` | body | `string` | no |
| `batch[].properties.contents[].content_category` | body | `string` | no |
| `batch[].properties.contents[].content_name` | body | `string` | no |
| `batch[].properties.contents[].brand` | body | `string` | no |
