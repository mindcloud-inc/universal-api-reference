# List Analytics Crawled Pages with Prerender.io

Retrieves analytics crawled pages from Prerender.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/analytics/crawled-pages`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [List Analytics Crawled Pages](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `adaptive_type` | query | `string` | no |
| `cache_hit` | query | `list<number>` | yes |
| `crawlers` | query | `list<string>` | yes |
| `date_from` | query | `string` | yes |
| `date_to` | query | `string` | yes |
| `domain` | query | `string` | no |
| `page` | query | `number` | no |
| `page_size` | query | `number` | no |
| `q` | query | `string` | no |
| `q_condition` | query | `string` | no |
| `response_time_high` | query | `number` | no |
| `response_time_low` | query | `number` | no |
| `sort` | query | `string` | no |
| `sort_direction` | query | `string` | no |
| `status_code` | query | `number` | no |
| `status_code_high` | query | `number` | no |
| `status_code_low` | query | `number` | no |
| `timedout` | query | `boolean` | no |
