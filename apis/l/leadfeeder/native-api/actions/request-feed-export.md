# Request Feed Export with Leadfeeder

Creates a custom feed export request in Leadfeeder.

## Endpoint

- **Method:** `POST`
- **Path:** `/export-requests`
- **Base URL:** `https://api.leadfeeder.com`
- **Official documentation:** [Request Feed Export](https://docs.leadfeeder.com/api/#request-a-feed-export)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `custom_feed_id` | body | `string` | yes |
| `start_date` | body | `date` | yes |
| `end_date` | body | `date` | yes |
