# Search GIFs with KLIPY

Finds GIFs in KLIPY by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/:app_key/gifs/search`
- **Base URL:** `https://api.klipy.com`
- **Official documentation:** [Search GIFs](https://docs.klipy.com/gifs-api/search-api)

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
