# List Trending GIFs with KLIPY

Retrieves current trending GIFs from KLIPY.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/:app_key/gifs/trending`
- **Base URL:** `https://api.klipy.com`
- **Official documentation:** [List Trending GIFs](https://docs.klipy.com/gifs-api/trending-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `number` | no |
| `per_page` | query | `number` | no |
| `customer_id` | query | `string` | yes |
| `locale` | query | `string` | no |
| `format_filter` | query | `string` | no |
