# Get Click Analytics with Linkly

Retrieves click analytics from Linkly.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspace/:workspace_id/clicks`
- **Base URL:** `https://app.linklyhq.com/api/v1`
- **Official documentation:** [Get Click Analytics](https://linklyhq.com/support/analytics-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `link_id` | query | `number` | no | The id of a single Link. |
| `link_ids` | query | `string` | no | Comma-separated list of Link IDs. |
| `start` | query | `string` | no | The start date for the date range. |
| `end` | query | `string` | no | The end date for the date range. |
| `country` | query | `string` | no | Filter clicks by country using ISO 3166-1 alpha-2 country code. |
| `browser` | query | `string` | no | Filter clicks by browser name. |
| `platform` | query | `string` | no | Filter clicks by platform or operating system. |
| `referer` | query | `string` | no | Filter clicks by referrer domain. |
| `isp` | query | `string` | no | Filter clicks by Internet Service Provider name. |
| `bots` | query | `boolean` | no | Set to false to exclude bot clicks from the results. |
| `unique` | query | `boolean` | no | Set to true to only include unique clicks in the results. |
| `timezone` | query | `string` | no | Timezone to use for date or time calculations. |
| `frequency` | query | `list` | no | Frequency of data points in the response. Accepted values: `day`, `hour`. |
