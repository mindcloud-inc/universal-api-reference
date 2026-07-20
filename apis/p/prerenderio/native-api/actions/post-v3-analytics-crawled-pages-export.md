# Create Analytics Crawled Pages Export with Prerender.io

Creates an analytics crawled pages export in Prerender.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/analytics/crawled-pages/export`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [Create Analytics Crawled Pages Export](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `adaptive_type` | body | `string` | no |
| `cache_hit` | body | `list<number>` | yes |
| `crawlers` | body | `list<string>` | yes |
| `date_from` | body | `string` | yes |
| `date_to` | body | `string` | yes |
| `domain` | body | `string` | no |
| `q` | body | `string` | no |
| `q_condition` | body | `string` | no |
| `response_time_high` | body | `number` | no |
| `response_time_low` | body | `number` | no |
| `sort` | body | `string` | no |
| `sort_direction` | body | `string` | no |
| `status_code` | body | `number` | no |
| `status_code_high` | body | `number` | no |
| `status_code_low` | body | `number` | no |
| `timedout` | body | `boolean` | no |
| `timezone` | body | `string` | no |
