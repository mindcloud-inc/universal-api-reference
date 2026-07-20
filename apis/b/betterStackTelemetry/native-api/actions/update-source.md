# Update Source with Better Stack Telemetry

Updates an existing telemetry source in Better Stack Telemetry.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/sources/:source_id`
- **Base URL:** `https://telemetry.betterstack.com`
- **Official documentation:** [Update Source](https://betterstack.com/docs/logs/api/update-source/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_id` | path | `string` | yes | ID of the source to update |
| `name` | body | `string` | no | Source name |
| `ingesting_paused` | body | `boolean` | no | Whether ingesting is paused for the source |
| `source_group_id` | body | `number` | no | Source group to attach the source to |
| `live_tail_pattern` | body | `string` | no | Pattern used for live tail display |
| `logs_retention` | body | `number` | no | Data retention for logs in days |
| `metrics_retention` | body | `number` | no | Data retention for metrics in days |
| `vrl_transformation` | body | `string` | no | VRL transformation to apply to ingested data |
| `scrape_urls[]` | body | `array<string>` | no | URLs to scrape for prometheus_scrape and similar platforms |
| `scrape_frequency_secs` | body | `number` | no | How often to scrape the URLs |
| `scrape_request_headers[]` | body | `array<object>` | no | Request headers for scrape requests as an array of objects with name and value |
| `scrape_request_basic_auth_user` | body | `string` | no | Basic auth username for scrape requests |
| `scrape_request_basic_auth_password` | body | `string` | no | Basic auth password for scrape requests |
