# List Trending Memes with KLIPY

Retrieves current trending memes from KLIPY.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/:app_key/static-memes/trending`
- **Base URL:** `https://api.klipy.com`
- **Official documentation:** [List Trending Memes](https://docs.klipy.com/memes-api/memes-trending-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customer_id` | query | `string` | yes |
| `format_filter` | query | `string` | no |
| `locale` | query | `string` | no |
| `page` | query | `string` | no |
| `per_page` | query | `string` | no |
