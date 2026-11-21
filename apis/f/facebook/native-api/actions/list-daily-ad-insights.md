# List Daily Ad Insights with Facebook

Retrieves daily spend, clicks, and conversion events for Meta ads.

## Endpoint

- **Method:** `GET`
- **Path:** `:adAccountId/insights`
- **Base URL:** `https://graph.facebook.com/v25.0`
- **Official documentation:** [List Daily Ad Insights](https://developers.facebook.com/docs/graph-api/reference/adaccount/insights/)

## Requirements

- **OAuth scopes:** `ads_read`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adAccountId` | path | `string` | yes | Enter the Meta ad account ID including the act_ prefix. |
| `since` | query | `string` | yes | Use YYYY-MM-DD. The date is included in the report. |
| `until` | query | `string` | yes | Use YYYY-MM-DD. The date is included in the report. |
