# Get Click Counts Grouped By Dimension with Linkly

Retrieves click counts by dimension from Linkly.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspace/:workspace_id/clicks/counters/:counter`
- **Base URL:** `https://app.linklyhq.com/api/v1`
- **Official documentation:** [Get Click Counts Grouped By Dimension](https://linklyhq.com/support/analytics-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `counter` | path | `list` | yes | The dimension to group clicks by. Accepted values: `country`, `isp`, `link_id`, `platform`, `referer`, `top_params`. |
| `link_id` | query | `number` | no | The id of a single Link. |
| `link_ids` | query | `string` | no | Comma-separated list of Link IDs. |
| `start` | query | `string` | no | The start date for the date range. |
| `end` | query | `string` | no | The end date for the date range. |
| `country` | query | `string` | no | Filter by country using ISO 3166-1 alpha-2 country code. |
| `bots` | query | `boolean` | no | Set to false to exclude bot clicks from the results. |
| `unique` | query | `boolean` | no | Set to true to only count unique clicks. |
