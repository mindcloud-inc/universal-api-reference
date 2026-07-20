# List Trending AI Emojis with KLIPY

Retrieves trending AI emojis from KLIPY.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/:app_key/emojis/trending`
- **Base URL:** `https://api.klipy.com`
- **Official documentation:** [List Trending AI Emojis](https://docs.klipy.com/emojis-api/emojis-trending-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customer_id` | query | `string` | yes |
| `format_filter` | query | `string` | no |
| `locale` | query | `string` | no |
| `page` | query | `string` | no |
| `per_page` | query | `string` | no |
