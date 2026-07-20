# Generate Keyword Historical Metrics with Google Ads

Generates keyword historical metrics in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId:generateKeywordHistoricalMetrics`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Generate Keyword Historical Metrics](https://developers.google.com/google-ads/api/reference/rpc/v22/KeywordPlanIdeaService/GenerateKeywordHistoricalMetrics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID to generate historical metrics for (without dashes). |
| `keywords[]` | body | `array<string>` | yes | Keywords for historical metrics lookup. |
| `language` | body | `string` | no | Resource name of the language constant. |
