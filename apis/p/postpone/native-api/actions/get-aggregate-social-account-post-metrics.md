# Get Aggregate Social Account Post Metrics with Postpone

Retrieves aggregate social account post metrics from Postpone.

## Endpoint

- **Method:** `POST`
- **Path:** `/gql`
- **Base URL:** `https://api.postpone.app`
- **Official documentation:** [Get Aggregate Social Account Post Metrics](https://developers.postpone.app/analytics/aggregate-social-account-post-metrics)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `variables.startDate` | body | `string` | yes |
| `variables.endDate` | body | `string` | yes |
| `variables.socialAccountIds[]` | body | `array<string>` | yes |
| `variables.metrics[]` | body | `array<string>` | yes |
