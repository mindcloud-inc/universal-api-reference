# Search Google Ads with Google Ads

Searches Google Ads using a custom GAQL query.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/googleAds:search`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Search Google Ads](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID to query (without dashes). |
| `query` | body | `string` | yes | GAQL query to execute. Use field names from the Google Ads Fields reference. |
| `startDate` | body | `string` | yes | Start date for the automatic segments.date filter (YYYY-MM-DD). |
| `endDate` | body | `string` | yes | End date for the automatic segments.date filter (YYYY-MM-DD). |
