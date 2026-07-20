# Create Source with Better Stack Telemetry

Creates a new telemetry source in Better Stack Telemetry.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/sources`
- **Base URL:** `https://telemetry.betterstack.com`
- **Official documentation:** [Create Source](https://betterstack.com/docs/logs/api/create-a-source/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Source name |
| `platform` | body | `string` | yes | Source platform |
| `team_name` | body | `string` | no | Required if using a global API token to specify the team that should own the source |
| `source_group_id` | body | `number` | no | Source group to attach the source to |
| `ingesting_paused` | body | `boolean` | no | Whether ingesting is paused for the source |
| `data_region` | body | `string` | no | Data region or private cluster name to create the source in |
| `live_tail_pattern` | body | `string` | no | Pattern used for live tail display |
| `logs_retention` | body | `number` | no | Data retention for logs in days |
| `metrics_retention` | body | `number` | no | Data retention for metrics in days |
| `vrl_transformation` | body | `string` | no | VRL transformation to apply to ingested data |
| `scrape_urls[]` | body | `array<string>` | no | URLs to scrape for prometheus_scrape and similar platforms |
| `scrape_frequency_secs` | body | `number` | no | How often to scrape the URLs |
| `scrape_request_headers[]` | body | `array<object>` | no | Request headers for scrape requests as an array of objects with name and value |
| `scrape_request_basic_auth_user` | body | `string` | no | Basic auth username for scrape requests |
| `scrape_request_basic_auth_password` | body | `string` | no | Basic auth password for scrape requests |
| `custom_bucket.name` | body | `string` | no | Name of the custom S3-compatible bucket |
| `custom_bucket.endpoint` | body | `string` | no | Endpoint for the custom S3-compatible bucket |
| `custom_bucket.access_key_id` | body | `string` | no | Access key ID for the custom bucket |
| `custom_bucket.secret_access_key` | body | `string` | no | Secret access key for the custom bucket |
| `custom_bucket.keep_data_after_retention` | body | `boolean` | no | Whether to keep data in the bucket after the retention period |
