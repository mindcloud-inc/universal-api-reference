# Get Post Time Series Metrics with Postpone

Retrieves post time series metrics from Postpone.

## Endpoint

- **Method:** `POST`
- **Path:** `/gql`
- **Base URL:** `https://api.postpone.app`
- **Official documentation:** [Get Post Time Series Metrics](https://developers.postpone.app/analytics/post-time-series-metrics)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `variables.startDate` | body | `string` | yes |
| `variables.endDate` | body | `string` | yes |
| `variables.socialAccountIds[]` | body | `array<string>` | no |
| `variables.metrics[]` | body | `array<string>` | no |
| `variables.groupBy` | body | `string` | no |
| `variables.subreddits[]` | body | `array<string>` | no |
