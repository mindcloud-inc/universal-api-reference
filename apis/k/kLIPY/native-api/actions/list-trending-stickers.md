# List Trending Stickers with KLIPY

Retrieves current trending stickers from KLIPY.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/:app_key/stickers/trending`
- **Base URL:** `https://api.klipy.com`
- **Official documentation:** [List Trending Stickers](https://docs.klipy.com/stickers-api/stickers-trending-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customer_id` | query | `string` | yes |
| `format_filter` | query | `string` | no |
| `locale` | query | `string` | no |
| `page` | query | `string` | no |
| `per_page` | query | `string` | no |
