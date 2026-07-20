# List Trending Clips with KLIPY

Retrieves current trending clips from KLIPY.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/:app_key/clips/trending`
- **Base URL:** `https://api.klipy.com`
- **Official documentation:** [List Trending Clips](https://docs.klipy.com/clips-api/clips-trending-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customer_id` | query | `string` | yes |
| `format_filter` | query | `string` | no |
| `locale` | query | `string` | no |
| `page` | query | `string` | no |
| `per_page` | query | `string` | no |
