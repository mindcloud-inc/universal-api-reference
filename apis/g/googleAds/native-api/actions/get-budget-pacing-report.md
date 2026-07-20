# Get Budget Pacing Report with Google Ads

Retrieves a budget pacing report from Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/googleAds:search`
- **Base URL:** `https://googleads.googleapis.com/`
- **Official documentation:** [Get Budget Pacing Report](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID to query (without dashes). |
| `startDate` | body | `string` | no | Optional start date (YYYY-MM-DD). |
| `endDate` | body | `string` | no | Optional end date (YYYY-MM-DD). |
| `filterClause` | body | `string` | no | Optional GAQL filter clause fragment without WHERE (advanced). |
