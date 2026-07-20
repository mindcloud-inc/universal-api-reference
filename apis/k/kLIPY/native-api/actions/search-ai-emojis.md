# Search AI Emojis with KLIPY

Finds AI emojis in KLIPY by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/:app_key/emojis/search`
- **Base URL:** `https://api.klipy.com`
- **Official documentation:** [Search AI Emojis](https://docs.klipy.com/emojis-api/emojis-search-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `content_filter` | query | `string` | no |
| `customer_id` | query | `string` | yes |
| `format_filter` | query | `string` | no |
| `locale` | query | `string` | no |
| `page` | query | `string` | no |
| `per_page` | query | `string` | no |
| `q` | query | `string` | no |
