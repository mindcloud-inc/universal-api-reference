# Get Aggregate Post Metrics with Postpone

Retrieves aggregate post metrics from Postpone.

## Endpoint

- **Method:** `POST`
- **Path:** `/gql`
- **Base URL:** `https://api.postpone.app`
- **Official documentation:** [Get Aggregate Post Metrics](https://developers.postpone.app/analytics/aggregate-post-metrics)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `variables.startDate` | body | `string` | yes |
| `variables.endDate` | body | `string` | yes |
| `variables.socialAccountIds[]` | body | `array<string>` | no |
| `variables.metrics[]` | body | `array<string>` | no |
| `variables.subreddits[]` | body | `array<string>` | no |
