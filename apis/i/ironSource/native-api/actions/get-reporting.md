# Get Reporting with ironSource

Retrieves reporting data from ironSource.

## Endpoint

- **Method:** `GET`
- **Path:** `levelPlay/reporting/v1`
- **Base URL:** `https://platform.ironsrc.com/`
- **Official documentation:** [Get Reporting](https://docs.unity.com/en-us/grow/levelplay/platform/api/reporting)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adFormat` | query | `string` | no | Optional ad format filter: rewarded, offerwall, interstitial, or banner. |
| `appKey` | query | `string` | no | Optional comma-separated application key filter. |
| `breakdowns` | query | `string` | no | Comma-separated breakdown list, defaulting to date when omitted. |
| `country` | query | `string` | no | Optional comma-separated ISO 3166-1 alpha-2 country codes. |
| `endDate` | query | `string` | no | Report end date in YYYY-MM-DD format, UTC timezone. |
| `metrics` | query | `string` | no | Comma-separated metric list, such as revenue,impressions,activeUsers. |
| `startDate` | query | `string` | no | Report start date in YYYY-MM-DD format, UTC timezone. |
