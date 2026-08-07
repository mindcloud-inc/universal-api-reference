# Generate Keyword Forecast Metrics with Google Ads

Generates keyword forecast metrics in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId:generateKeywordForecastMetrics`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Generate Keyword Forecast Metrics](https://developers.google.com/google-ads/api/reference/rpc/v22/KeywordPlanIdeaService/GenerateKeywordForecastMetrics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID to generate forecast metrics for (without dashes). |
| `campaign` | body | `object` | yes | Campaign definition used for keyword forecast metrics. |
